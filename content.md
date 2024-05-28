# Desvendando os Iteradores em Python: Uma Introdução Completa

## O que são Iterators de Python

Se você está começando com Python, provavelmente já ouviu falar de iteradores, mas pode não estar muito certo do que eles são. Basicamente, um iterador é um objeto que permite percorrer uma sequência de valores, como uma lista ou uma tupla, um elemento de cada vez, sem precisar saber o tamanho dessa sequência de antemão. Isso significa que, com um iterador, você pode processar dados sem carregar toda a coleção na memória de uma vez, o que é muito eficiente.

## Qual sua tarefa no código

Os iteradores são como um controle remoto para navegar em uma coleção de itens. Eles ajudam a percorrer listas, tuplas, dicionários e até mesmo arquivos de forma eficiente. Você não precisa de um índice ou de um loop for complicado. É só usar o iterador para ir de um item ao próximo com o método __next__(). Como mostra no exemplo abaixo:

``` Python
frutas = ['maçã', 'banana', 'cereja']
iterador = iter(frutas)

print(next(iterador))  # Saída: maçã
print(next(iterador))  # Saída: banana
print(next(iterador))  # Saída: cereja
```

Aqui, usamos __iter()__ para criar um iterador e __next()__ para obter os itens um a um.

## Quais seus pontos mais fortes vs mais fracos

Os iteradores são ótimos porque economizam memória e tornam seu código mais limpo e legível. Você pode processar grandes quantidades de dados sem os carregar todos na memória de uma vez. No entanto, eles têm suas desvantagens, como não permitir voltar ao início da sequência sem reiniciar o iterador

### Vantagens

Uma grande vantagem dos iteradores é a eficiência no uso de memória. Em vez de carregar uma lista enorme de números na memória, você pode processar cada número um de cada vez:

``` Python
numeros = range(1000000)
iterador = iter(numeros)

for _ in range(10):
    print(next(iterador))
```

Aqui, criamos um iterador para uma sequência de um milhão de números. O loop imprime apenas os primeiros 10 números. Mesmo que a sequência seja gigantesca, o iterador mantém apenas um item na memória por vez.

### Desvantagens

Uma desvantagem dos iteradores é que eles são unidirecionais. Uma vez que você avançou para o próximo item, não pode voltar sem reiniciar o iterador:

``` Python
frutas = ['maçã', 'banana', 'cereja']
iterador = iter(frutas)

print(next(iterador))  # Saída: maçã
print(next(iterador))  # Saída: banana
```

- __Não há__ como voltar ao início sem criar um novo iterador

iterador = iter(frutas)
print(next(iterador))  # Saída: maçã

Após avançar no iterador, para voltar ao início, você precisa criar um novo iterador. No exemplo acima, após avançar para 'maçã' e 'banana', recriamos o iterador para voltar ao início e imprimir 'maçã' novamente. Isso pode ser inconveniente em certas situações onde a capacidade de voltar é necessária.

## Conclusão

Curtiu aprender sobre iteradores em Python? Ele foi gerado por inteligência artificial, porém revisado por alguém __100%__ Humano! Me acompanhe nas redes sociais para não perder nenhuma novidade e se aprofundar ainda mais no mundo Tech.

- [LinkedIn](https://www.linkedin.com/in/matheussantossi/)
- [GitHub](https://github.com/MatheusDSantossi)

Fontes de produção
Ilustrações de capa: gerada pela [lexica.art](https://lexica.art)
Conteúdo gerado por: [ChatGPT](https://chatgpt.com) e revisões humanas.

Link para o artigo na [DIO](https://web.dio.me/articles/artigo-desvendando-os-iteradores-em-python-uma-introducao-completa?back=%2Farticles&open-modal=true&page=1&order=oldest)

> #Python #Iterators #DataScience
