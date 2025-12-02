## Make Bundled discount compatible with RealOnePageCheckout plugin(nopTemplate).

To make Bundled discount plugin compatible with RealOnePageCheckout Plugin of nopTemplate you need to follow few steps as below:

Step:1

Add id="sub-total" In

SevenSpikes.Nop.Plugins.RealOnePageCheckout\Views\RealOnePageCheckout\OrderTotals.cshtml

Go to first <tr> row section of table as shown in below image:

![Test](../assets/img/BundleDiscount_Code1.png)

Step:2
Add id="real-onepage-total" In SevenSpikes.Nop.Plugins.RealOnePageCheckout\Views\RealOnePageCheckout\OrderTotals.cshtml

Go to <tr class="order-total"> </tr> section as shown in below image:

![Test](../assets/img/BundleDiscount_Code2.png)

Step:3

Go to SevenSpikes.Nop.Plugins.RealOnePageCheckout\Views\RealOnePageCheckout\OrderTotals.cshtml and add following script in end of the page.

```html
<script>

    //ajax-call on SubTotal value change
    var orderSubTotal = document.getElementById('sub-total');
    var UpdateOrderSummary = {
        Url: '@Url.Action("UpdateRealOnePageCheckoutOrderSummary", "BundledDiscounts")'
    }
    orderSubTotal.addEventListener('DOMSubtreeModified', UpdateOrderSection);

    function UpdateOrderSection(e) {
        $.ajax({
            url: UpdateOrderSummary.Url,
            type: "POST",
            success: function (result) {
                if (result.Success) {

                    if (result.BundledDiscount == "") {
                        $('.order-bundle-discount').hide();
                    }
                    else {

                        if (!$(".cart-total tbody tr:first").hasClass('sub-total-row')) {
                            $(".cart-total tbody tr:first").addClass('sub-total-row');
                        }

                        var bundleHtml = "<tr class='order-bundle-discount'><td class='cart-total-left'>@T(\"Nop.Plugin.XcellenceIt.BundledDiscounts.Totals.BundleDiscount\"):</label >"
                            + "</td><td class='cart-total-right'>"
                            + "<span id='bundled-discount-amount' class='value-summary'>-" + result.BundledDiscount + "</span>"
                            + "</td></tr>";

                        $(".order-bundle-discount").remove();
                        $('.sub-total-row').after(bundleHtml);
                        $('.order-bundle-discount').show();
                    }

                    if ($('#real-onepage-total') != null) {
                        $('#real-onepage-total').html(result.OrderTotal);
                    }
                }
            }
        });
    }

</script>

```