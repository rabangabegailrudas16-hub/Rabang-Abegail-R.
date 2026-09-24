
# Research on Cloud Storage Types

## Comparison of Storage Types

| Storage Type | Description | Primary Use Case | Cloud Provider Example |
|---|---|---|---|
| Block Storage | Data is divided into blocks and stored on storage volumes that can be attached to computing resources. | Databases, virtual machines, and applications requiring low-latency storage. | AWS EBS |
| File Storage | Data is kept as files inside folders and directories using a file-system structure. | Shared folders, file servers, and applications that require file-system access. | AWS EFS |
| Object Storage | Data is stored as individual objects together with metadata and a unique identifier inside buckets. | Images, videos, documents, backups, and other unstructured data. | AWS S3 |

## Recommendation for the Client

Object Storage is appropriate for the photo-sharing application because photos are unstructured files that can be stored as individual objects. It can also handle a very large number of files and allows the storage capacity to grow as more users upload photos.
