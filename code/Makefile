.PHONY: all

ifndef INPUT_FILE
INPUT_FILE = ../data/dev.json
endif

ifndef OUTPUT_DIR
OUTPUT_DIR = predictions/
endif

roberta: colake

roberta-base:
	python3 eval_discriminative_models.py --pretrained-class roberta-base --tokenizer RobertaTokenizer --intrasentence-model RoBERTaLM --intersentence-model ModelNSP --skip-intersentence --intersentence-load-path models/pretrained_models/RobertaModel_roberta-base_1e-05.pth --input-file $(INPUT_FILE) --output-dir $(OUTPUT_DIR) $(FLAGS)

colake:
	python3 eval_discriminative_models.py --pretrained-class roberta-base --tokenizer RobertaTokenizer --intrasentence-model CoLake --intrasentence-load-path ../../colake-bias/model/model.bin --skip-intersentence --intersentence-model ModelNSP --input-file $(INPUT_FILE) --output-dir $(OUTPUT_DIR) $(FLAGS)