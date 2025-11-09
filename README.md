import matplotlib.pyplot as plt
import matplotlib as mpl
import numpy as np

PALETA = {
    "linha": "#1f77b4",                 
    "linha_marker_edge": "#0b3d91",     
    "barras": ["#1f77b4", "#ff7f0e", "#2ca02c", "#9467bd"],  
    "pizza": ["#66b3ff", "#99ff99", "#ffcc99"],
    "scatter_colors": ["red", "orange", "green", "blue", "purple"],
    "scatter_cmap": "viridis"           
}


dias = [1, 2, 3, 4, 5, 6, 7]
estoque = [100, 95, 110, 105, 120, 115, 130]

plt.figure(figsize=(8, 4.5))
plt.plot(
    dias, estoque,
    color=PALETA["linha"],
    marker='o',
    markerfacecolor=PALETA["linha"],
    markeredgecolor=PALETA["linha_marker_edge"],
    linestyle='-', linewidth=2,
    label='Quantidade'
)
plt.title("Tendência de Estoque Diário")
plt.xlabel("Dia")
plt.ylabel("Quantidade em Estoque")
plt.grid(True, linestyle='--', alpha=0.5)
plt.legend()
plt.show()


produtos = ['Teclado', 'Mouse', 'Monitor', 'Webcam']
quantidades = [50, 75, 30, 60]

plt.figure(figsize=(8, 4.5))

plt.bar(produtos, quantidades, color=PALETA["barras"])
plt.title("Comparação de Estoque por Produto")
plt.xlabel("Produto")
plt.ylabel("Quantidade")

for i, valor in enumerate(quantidades):
    plt.text(i, valor + 1.5, str(valor), ha='center', fontsize=9)
plt.show()


categorias = ['Eletrônicos', 'Vestuário', 'Alimentos']
valores = [15000, 8000, 5000]

plt.figure(figsize=(6.5, 6.5))
plt.pie(
    valores,
    labels=categorias,
    autopct='%1.1f%%',
    colors=PALETA["pizza"],
    startangle=90,
    wedgeprops={'edgecolor': 'white'}
)
plt.title("Proporção do Valor em Estoque por Categoria")
plt.show()


precos = np.array([50, 120, 300, 80, 20])
estoque_itens = np.array([80, 25, 10, 70, 150])

plt.figure(figsize=(8, 4.5))

plt.scatter(precos, estoque_itens, c=PALETA["scatter_colors"], s=100, edgecolor='black', label='Itens (cores categóricas)')


plt.title("Preço x Quantidade em Estoque")
plt.xlabel("Preço Unitário (R$)")
plt.ylabel("Quantidade")
plt.grid(True, linestyle='--', alpha=0.5)
plt.legend()
plt.show()
