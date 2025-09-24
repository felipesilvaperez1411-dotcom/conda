#!/bin/bash
conda create -n mi_entorno python=3.10 -y
conda activate mi_entorno
echo 'numeros = [1, 2, 3, 4, 5]
palabras = ["manzana", "banana", "cereza"]

print("Lista de números:", numeros)
print("Lista de palabras:", palabras)' > mi_codigo.py
python mi_codigo.py
