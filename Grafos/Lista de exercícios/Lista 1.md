[[ComputerScience/Grafos/Introdução|Introdução]]
##### Exercício 38
![[Pasted image 20250828103912.png]]

```c
#include <math.h>
#include <stdio.h>

double f(double x) {
	double resultado;
	resultado = pow(x,2);
	return resultado;
}

double g(double x) {
	double resultado = log10(x);
	return resultado;
}

double w(double x) {
	double resultado = 2 * x - 1;
	return resultado;
}

double h(double x) {
	double resultado = pow(3,x);
	return resultado;
}

int main() {
	double num, f_f, f_g, f_w, f_h;
	printf("Digite um número");
	scanf("%lf", &num);
    
    f_f = f(num);
    f_g = g(f_f);
    f_w = w(f_g);
    f_h = h(f_w);
	
    printf("f(x) = %lf\n", f_f);
    printf("g(f(x)) = %lf\n", f_g);
    printf("w(g(f(x))) = %lf\n", f_w);
    printf("h(w(g(f(x)))) = %lf\n", f_h);


	return 0;
}
```