# Create Directory milvus
```sh
mkdir milvus
cd milvus
```

# Download the installation script
```sh
wget https://raw.githubusercontent.com/milvus-io/milvus/master/scripts/standalone_embed.sh
```

# Start the Docker container
```sh
bash standalone_embed.sh start
```

# Stop Milvus
```sh
bash standalone_embed.sh stop
```

# Delete Milvus data
```sh
bash standalone_embed.sh delete
```

# Test script `1.py`
```python
from pymilvus import connections, MilvusException

try:
    print("=== start connecting to Milvus ===")
    connections.connect("default", host="127.0.0.1", port="19530")
    print("Connected to Milvus successfully!")
except MilvusException as e:
    print(f"Failed to connect to Milvus: {e}")
```

# Run the script
```sh
python3 1.py
```
