# Facet Filter with % does not work

## **Question**

When I apply a facet that contains the **%** character, the facet results are not displayed correctly.

---

## **Solution**

Solr does **not support using `%` inside facet values`**.  
If your facet value contains a **%**, Solr may fail to process it, causing the facet filter to behave incorrectly.

To fix this:

- **Avoid using `%`** in facet values.
- Rename or clean the facet data to remove the `%` symbol.

Once the `%` character is removed, faceting will work properly again.

[← Previous](SearchWithSynonyms.md) | [Next →](SolrService.md)