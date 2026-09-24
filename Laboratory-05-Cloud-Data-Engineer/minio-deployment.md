
# MinIO Deployment Documentation

## Deployment Method

MinIO was installed and started as a Docker container in the KillerCoda Ubuntu environment. Docker was used to simplify the setup and avoid manually installing the MinIO server and its dependencies.

## Docker Command

The following command was executed:

```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
-e "MINIO_ROOT_USER=cloudadmin" \
-e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
quay.io/minio/minio server /data --console-address ":9001"
```

## Port Configuration

Two ports were mapped during deployment.

- **Port 9000** - MinIO API
- **Port 9001** - MinIO Web Console

The browser-based administration console was accessed through port **9001**.

## Administrator Credentials

The Docker command configured the MinIO administrator account using environment variables.

Username:

```text
cloudadmin
```

Password:

```text
CloudNova2026!
```

## Environment Variables

The `-e` options define configuration values that are passed into the MinIO container.

The first variable was:

```text
MINIO_ROOT_USER=cloudadmin
```

This specifies the root administrator username.

The second variable was:

```text
MINIO_ROOT_PASSWORD=CloudNova2026!
```

This specifies the password for the root administrator account.

## Object Storage Bucket

A bucket named:

```text
client-photos
```

was created through the MinIO Web Console.

A sample file was then uploaded to the bucket to verify that objects could be stored successfully.

## Container Verification

The following command was used to check the running Docker containers:

```bash
docker ps
```

The output confirmed that the MinIO container was active and that the required ports were mapped.
