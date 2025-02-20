BIN_DIR  := bin/
INC_DIR  := inc/
SRC_DIR  := src/
OBJ_DIR  := obj/
CC := gcc
CFLAGS := -Wall
LDFLAGS=-lm -lpthread -lrt
WIPI := -l wiringPi

# Arquivos serão colocados 
SRCFILES := $(wildcard $(SRC_DIR)*.c)
INCFILES := $(wildcard $(INC_DIR)*.c)

# Cria uma lista de binários correspondentes aos arquivos .c
BINS := $(SRCFILES:$(SRC_DIR)%.c=$(BIN_DIR)%)

# Alvo padrão
all: $(BINS)

# Regra para gerar cada binário individualmente
$(BIN_DIR)%: $(OBJ_DIR)%.o
	$(CC) $(CFLAGS) $< $(INCFILES) -o $@ $(L
# Regra para gerar o arquivo objeto .o a partir do arquivo .c
$(OBJ_DIR)%.o: $(SRC_DIR)%.c
	$(CC) $(CFLAGS) -c $< -o $@ -I./$(INC_DIR)

#phony -> Aplicado para o make não confundir comandos com nomes de arquivos
.PHONY: clean run 
clean:
	rm -rf obj/*
	rm -rf bin/*

# run:
# 	$(BIN_DIR)*/
