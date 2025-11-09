import matplotlib.pyplot as plt

# 1. Gráfico de Linha - Tendência de Estoque Diário 
dias = [1, 2, 3, 4, 5, 6, 7]
estoque = [100, 95, 110, 105, 120, 115, 130]

plt.plot(dias, estoque, color='green', marker='s', linestyle='--', linewidth=2)  # Cor alterada para verde e marcador quadrado
plt.title("Tendência de Estoque Diário - Modificado", fontsize=12)
plt.xlabel("Dia")
plt.ylabel("Quantidade em Estoque")
plt.grid(True, linestyle=':', alpha=0.7)  # Alteração no estilo da grade
plt.savefig("grafico_linha_modificado.png")  # Salva o gráfico como arquivo
plt.show()


# 2. Gráfico de Barras - Comparação de Produtos 
produtos = ['Teclado', 'Mouse', 'Monitor', 'Webcam']
quantidades = [50, 75, 30, 60]
cores = ['#ff6347', '#4682b4', '#32cd32', '#ff1493']  # Cores alteradas para outras tonalidades

plt.bar(produtos, quantidades, color=cores)
plt.title("Comparação de Estoque por Produto - Modificado", fontsize=12)
plt.xlabel("Produto")
plt.ylabel("Quantidade")
for i, valor in enumerate(quantidades):
    plt.text(i, valor + 2, str(valor), ha='center', fontsize=9)
plt.savefig("grafico_barras_modificado.png")  # Salva o gráfico como arquivo
plt.show()


# 3. Gráfico de Pizza - Proporção de Categorias 
categorias = ['Eletrônicos', 'Vestuário', 'Alimentos']
valores = [15000, 8000, 5000]
cores_pizza = ['#ffb6c1', '#add8e6', '#ffdab9']  # Cores alteradas para tons pastéis

plt.pie(valores, labels=categorias, autopct='%1.1f%%', colors=cores_pizza, startangle=90)
plt.title("Proporção do Valor em Estoque por Categoria - Modificado", fontsize=12)
plt.savefig("grafico_pizza_modificado.png")  # Salva o gráfico como arquivo
plt.show()


# 4. Gráfico de Dispersão - Preço vs Quantidade 
precos = [50, 120, 300, 80, 20]
estoque_itens = [80, 25, 10, 70, 150]
cores_pontos = ['cyan', 'magenta', 'yellow', 'black', 'gray']  # Cores alteradas para tons diferentes

plt.scatter(precos, estoque_itens, c=cores_pontos, s=100, edgecolor='white')  # Aumentei o tamanho dos pontos
plt.title("Preço x Quantidade em Estoque - Modificado", fontsize=12)
plt.xlabel("Preço Unitário (R$)")
plt.ylabel("Quantidade")
plt.grid(True, linestyle=':', alpha=0.7)  # Alteração no estilo da grade
plt.savefig("grafico_dispercao_modificado.png")  # Salva o gráfico como arquivo
plt.show()
