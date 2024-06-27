# LLMs-RAG
pip install tqdm notebook==7.1.2 openai elasticsearch pandas scikit-learn ipywidgets
Implementing an augmented search using LLMs
docker run -it \
    --rm \
    --name elasticsearch \
    -p 9200:9200 \
    -p 9300:9300 \
    -e "discovery.type=single-node" \
    -e "xpack.security.enabled=false" \
    docker.elastic.co/elasticsearch/elasticsearch:8.4.3
