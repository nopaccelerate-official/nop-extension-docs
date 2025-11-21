# Implement WebRequest for `StartIndexing` Method

## **Questions**
How do you implement a WebRequest for the **StartIndexing** method?

**Solution:**

StartIndexing is an async method so if you request it, it will work in background & will not impact your website traffic.

**Implementing StartIndexing GET method in a third-party tool:**

```csharp
string webAddr = <DomainName>/Admin/NopAcceleratePlusSearch/StartIndexing;

var httpWebRequest = (HttpWebRequest)WebRequest.Create(webAddr);
httpWebRequest.ContentType = "application/json";
httpWebRequest.Method = "GET";

HttpWebResponse httpResponse = (HttpWebResponse)httpWebRequest.GetResponse();

if (httpResponse.StatusCode == HttpStatusCode.OK)
{
    using (var streamReader = new StreamReader(httpResponse.GetResponseStream()))
    {
        var responseText = streamReader.ReadToEnd();
    }
}
```


## Notes

Call this method after your updates are completed using any third-party tool, external script, or integration so your catalog achieves **100% indexing**.


[← Previous](FontError.md) | [Next →](Help.md)

