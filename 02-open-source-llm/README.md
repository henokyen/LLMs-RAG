pip install tqdm notebook==7.1.2 openai elasticsearch pandas scikit-learn ipywidgets 
pip install python-dotenv

https://huggingface.co/google/flan-t5-xl
Explanation of Parameters:

max_length: Set this to a higher value if you want longer responses. For example, max_length=300.
num_beams: Increasing this can lead to more thorough exploration of possible sequences. Typical values are between 5 and 10.
do_sample: Set this to True to use sampling methods. This can produce more diverse responses.
temperature: Lowering this value makes the model more confident and deterministic, while higher values increase diversity. Typical values range from 0.7 to 1.5.
top_k and top_p: These parameters control nucleus sampling. top_k limits the sampling pool to the top k tokens, while top_p uses cumulative probability to cut off the sampling pool. Adjust these based on the desired level of randomness.

the best way to run llms on local computer is to use
https://github.com/ollama/ollama

these are the steps to install and run ollam on linux machine
1/ curl -fsSL https://ollama.com/install.sh | sh
2. ollama start
ollama pull phi3
ollama run phi3

to run ollam on a docker use the following command

docker run -it \
    -v ollama:/root/.ollama \
    -p 11434:11434 \
    --name ollama \
    ollama/ollama

use the following command to see if port 11434 is occupied or free
sudo lsof -i :11434