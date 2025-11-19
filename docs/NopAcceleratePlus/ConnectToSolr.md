# How can I connect to Solr?

## **Question**

How can I connect to Solr? It shows a connection issue.

---

## **Solution**

First, verify that your **Solr Core URL** is correct.

### Example
If your Solr core name is **Solr_sample**, then your Solr Core URL should be:
http://localhost:8983/solr/Solr_sample


---

## **Make Sure:**

- Your Solr Core URL **does not end with a `/`**  
  *Correct:* `http://localhost:8983/solr/Solr_sample`  
  *Incorrect:* `http://localhost:8983/solr/Solr_sample/`

- Remove **`#`** from the Solr Core URL if it exists.

