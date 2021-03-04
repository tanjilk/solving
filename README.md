


# Solving
## Resolução de vários exercícios e algoritmos em linguagem C/C++

 - [Módulo 1](#primeiro-modulo)
 - [Módulo 2](#segundo-modulo)
 	- Condições com IF ELSEIF ELSE 
 	- Ciclos FOR WHILE DO WHILE
 	- Descobrir números primos
 	- Indicar os divisores etc...
 - [Módulo 3](#terceiro-modulo)
 	- Funções void e com tipo de dado
 - [Módulo 4](#quarto-modulo)
 	- Arrays, vetores, matrizes multidimensionais
 
 

### Primeiro Modulo
Introdução á algoritmia e fluxogramas, problemas de algoritmia em C++

 1. [Ficha Prática](https://github.com/tanjilk/solving/blob/master/m%C3%B3dulo%201/Ficha%20pra%CC%81tica%2001.pdf)
 2. [Ficha Prática](https://github.com/tanjilk/solving/blob/master/m%C3%B3dulo%201/Ficha%20pra%CC%81tica%2002.pdf)
 3. [Ficha Prática](https://github.com/tanjilk/solving/blob/master/m%C3%B3dulo%201/Ficha%20pra%CC%81tica%2003.pdf)

### Segundo Modulo
Introdução em linguagem C/C++ com as condições IF  ELSE IF ELSE e ciclos FOR WHILE DO WHILE
  - [Ficha Avaliação](https://github.com/tanjilk/solving/blob/master/m%C3%B3dulo%202/Teste01.pdf)
  - [Resolução](https://github.com/tanjilk/solving/blob/master/m%C3%B3dulo%202/sistema_compras_vendas.cpp)  
  
Sistema de Compras e Vendas

### Terceiro Modulo
Funções void e funções com tipos de dados
Algoritmos que possam ser implementadas nos próximos exercícios
Descobrir números primos, encontrar divisores etc...

#### Numeros Primos
Exemplo de um exercício seguinte
Escrever uma função em C++ que imprima os N primeiros números primos. O valor de N tem que ser maior que 10 e menor que 100. Qualquer valor fora deste intervalo deve imprimir o texto "Não é possivel realizar essa operação"
```cpp
void primo(int n){
    if(n < 10 || n > 100){
        std::cout << "Nao e possivel realizar essa operacao";
    } else {
        for(int i = 1; i<=n; i++){
            int divisor = 2;
            while(i % divisor != 0){
                divisor++;
            }
            if(divisor == i){
                std::cout << i << ", ";
            }
        }
    }
}
```
Verificar se é primo ou não
```cpp
	int num;
    int c = 0;
    
    std::cout << "Introduze o numero: ";
    std::cin >> num;

    for(int i = 1; i<=num; i++){
        if(num % i == 0){
            c++;
        }
    }
    if(c == 2){
        std::cout << "É primo";
    } else {
        std::cout << "Nao é primo";
    }
```

Verificar se é primo ou não utilizando um ciclo while
```cpp
int primo(int num){
    int n;
    for(int i = 1; i<=num; i++){
        if(num % i == 0){
            n++;
        }
    }
    if(n == 2){
        return 1;
    } else {
        return -1;
    }
}
```
Mostrar primeiros numeros primos ate 50
```cpp
for(int i = 1; i<=50; i++){
        int divisor = 2;
        while(i % divisor != 0){
            divisor++;
        }
        if(divisor == i){
            std::cout << i << std::endl;
        }
    }    
```
Imprimir 10 primeiros multiplos de 5
```cpp
for(int i = 1; i<=10; i++){
        cout << i * 5;
    }
```

Dado um número, indicar os divisores de um número
```cpp
int num;
std::cin >> num;
for(int i = 1; i<=num; i++){
	if(num % i == 0){
		std::cout << i << ", ";
    }
}
```

### Quarto Modulo
Arrays, Vetores, Vetores multidimensionais e Matrizes


#### Vetores
Para criar um simples vetor
`int vet[15];`

Preenchendo um vetor á medida que o utilizador vai introduzir valores
```cpp
for(int i = 0; i<n; i++){
		
	std::cout << "Introduze o valor da posicao " << i;
	std::cin >> vet[i];

}
```

Funções para mostrar vetores e usa las em main
```cpp
void mostrar_vetor(int vet[], int n){
	for(int i = 0; i<n; i++){
		std::cout << vet[i];
	}
}


int main(){
	
	int vet[15];
	preencher_vetor(vet, 15);
	mostrar_vetor(vet, 15);
}
```

#### Matrizes

Matrizes é literalmente um vetor e nesse vetor tem vetores por exemplo vamos criar uma matriz de 2x2.
```cpp
int matriz[2][2] = {
	{1,2},
	{3,4}
};
```

Lendo uma matriz de 4x4
```cpp
int matriz[4][4];
for(int linha = 0; linha < 4; linha++){
	for(int coluna = 0; coluna < 4; coluna++){
		cin >> matriz[linha][coluna];
	}
}
```

Bubble Sort
![gif](https://miro.medium.com/max/1992/1*Xf5HAp0lN-6qHsziRnjVxg.gif)
