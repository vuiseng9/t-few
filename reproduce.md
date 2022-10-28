
conda create -n tfew python==3.8

git clone https://github.com/vuiseng9/t-few

pip3 install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu116

pip install -r requirements.txt

source bin/start.sh
CUDA_VISIBLE_DEVICES=3 python -m src.pl_train -c t03b.json+rte.json -k save_model=False exp_name=first_exp