# Setup Solr on Docker

## 1. Directory Setup 

### 1.1 Windows Setup

Create directory: **C:\Docker-data\Solr-volume**

Inside this directory create:
**C:\Docker-data\Solr-volume\lib**

Place JDBC driver inside:
`sqljdbc822.jar`

**Note: This driver is required for SQL Server integration using Solr DataImportHandler.**

## 2. Linux Setup

### 2.1 Directory Creation

Create directory:
`mkdir -p /root/solr/solr-data/lib`

### 2.2 Permissions (IMPORTANT)

```
chown -R 8983:8983 /root/solr/solr-data
chmod -R 755 /root/solr/solr-data 
```

**Explanation:** Solr container runs as UID 8983. Without permission fixes, Solr cannot write data.

---

## 3. Docker Compose Configuration

### 3.1 Windows docker-compose.yml

```yaml
version: '3.8'
services:
  solr:
    image: solr:8.11
    container_name: solr_server
    ports:
      - "8983:8983"
    environment:
      - SOLR_HOME=/var/solr/data
    volumes:
      - "C:/Docker-data/Solr-volume:/var/solr/data"
    command: solr-foreground
    restart: unless-stopped
```
Run: docker compose up -d

### 3.2 Linux docker-compose.yml

```yaml
version: '3.8'
services:
  solr:
    image: solr:8.11
    container_name: solr_server
    ports:
      - "8983:8983"
    environment:
      - SOLR_HOME=/var/solr/data
    volumes:
      - /root/solr/solr-data:/var/solr/data
    command: solr-foreground
    restart: unless-stopped
```
Run: docker compose up -d

##**4. Verify Solr Installation**
**Open browser: http://localhost:8983**

Expected result: Solr Admin UI dashboard.

**Check container logs:**
```docker logs solr_server```

##**5. Add JDBC Driver Configuration**
If using SQL Server integration:

**Copy sqljdbc822.jar to:**
```/var/solr/data/lib/```

**Modify solrconfig.xml and add:**
```<lib dir="/var/solr/data/lib/" regex="sqljdbc822.jar" />```

Restart container:
```docker restart solr_server```

##**6. Create Solr Core**
**Create core:**
```docker exec -it solr_server solr create -c mycore```

Verify in UI → Core Admin → mycore.

##**7. Create Additional Cores**
**To create more cores:**
```docker exec -it solr_server solr create -c newcore```

Each core will be stored in the persistent volume automatically.

##**8. Troubleshooting**
- Permission denied: Fix Linux permissions again.
- Container not starting: docker logs solr_server
- Port conflict: Change host port in docker-compose.yml.

##**9. Production Recommendations (Optional)**
- Use resource limits
- Enable monitoring
- Configure backups
- Use version pinning

**Example resource limits:**

```yaml
deploy:
  resources:
    limits:
      memory: 2g
```

###**10. Stop Solr**
docker compose down

[← Previous](SetupCoreOnSharedServer.md) | [Next →](version-history.md)