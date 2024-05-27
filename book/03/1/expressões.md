{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Expressões\n",
    "\n",
    "As linguagens de programação são muito mais simples do que as linguagens humanas. No entanto, existem algumas regras de gramática para aprender em qualquer linguagem, e é por aí que começaremos. Neste texto, usaremos a linguagem de programação [Python](https://www.python.org/). Aprender as regras de gramática é essencial, e as mesmas regras usadas nos programas mais básicos também são centrais para os programas mais sofisticados.\n",
    "\n",
    "Os programas são compostos por *expressões*, que descrevem para o computador como combinar partes de dados. Por exemplo, uma expressão de multiplicação consiste em um símbolo `*` entre duas expressões numéricas. As expressões, como `3 * 4`, são *avaliadas* pelo computador. O valor (o resultado da *avaliação*) da última expressão em cada célula, `12` neste caso, é exibido abaixo da célula."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 1,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "12"
      ]
     },
     "execution_count": 1,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "3 * 4"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "As regras de gramática de uma linguagem de programação são rígidas. No Python, o símbolo `*` não pode aparecer duas vezes seguidas. O computador não tentará interpretar uma expressão que difere de suas estruturas de expressão prescritas. Em vez disso, mostrará um erro `SyntaxError`. A *sintaxe* de uma linguagem é seu conjunto de regras gramaticais, e um `SyntaxError` indica que uma estrutura de expressão não corresponde a nenhuma das regras da linguagem."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 2,
   "metadata": {
    "tags": [
     "raises-exception"
    ]
   },
   "outputs": [
    {
     "ename": "SyntaxError",
     "evalue": "invalid syntax (<ipython-input-2-012ea60b41dd>, line 1)",
     "output_type": "error",
     "traceback": [
      "\u001b[0;36m  File \u001b[0;32m\"<ipython-input-2-012ea60b41dd>\"\u001b[0;36m, line \u001b[0;32m1\u001b[0m\n\u001b[0;31m    3 * * 4\u001b[0m\n\u001b[0m        ^\u001b[0m\n\u001b[0;31mSyntaxError\u001b[0m\u001b[0;31m:\u001b[0m invalid syntax\n"
     ]
    }
   ],
   "source": [
    "3 * * 4"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Pequenas alterações em uma expressão podem mudar completamente seu significado. Abaixo, o espaço entre os `*` foi removido. Como `**` aparece entre duas expressões numéricas, a expressão é uma *expressão de exponenciação* bem formada (o primeiro número elevado à potência do segundo: 3 vezes 3 vezes 3 vezes 3). Os símbolos `*` e `**` são chamados *operadores*, e os valores que eles combinam são chamados *operandos*."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "81"
      ]
     },
     "execution_count": 3,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "3 ** 4"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Operadores Comuns.** A ciência de dados frequentemente envolve a combinação de valores numéricos, e o conjunto de operadores em uma linguagem de programação é projetado para que as expressões possam ser usadas para expressar qualquer tipo de aritmética. No Python, os seguintes operadores são essenciais.\n",
    "\n",
    "| Tipo de Expressão | Operador | Exemplo    | Valor     |\n",
    "|-----------------|----------|------------|-----------|\n",
    "| Adição        | `+`      | `2 + 3`    | `5`       |\n",
    "| Subtração     | `-`      | `2 - 3`    | `-1`      |\n",
    "| Multiplicação  | `*`      | `2 * 3`    | `6`       |\n",
    "| Divisão        | `/`      | `7 / 3`    | `2.66667` |\n",
    "| Resto       | `%`      | `7 % 3`    | `1`       |\n",
    "| Exponenciação  | `**`     | `2 ** 0.5` | `1.41421` |"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "As expressões em Python obedecem às mesmas regras familiares de *precedência* que na álgebra: multiplicação e divisão ocorrem antes da adição e subtração. Parênteses podem ser usados para agrupar expressões menores dentro de uma expressão maior."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "17.555555555555557"
      ]
     },
     "execution_count": 4,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "1 + 2 * 3 * 4 * 5 / 6 ** 3 + 7 + 8 - 9 + 10"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 5,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "2017.0"
      ]
     },
     "execution_count": 5,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "1 + 2 * (3 * 4 * 5 / 6) ** 3 + 7 + 8 - 9 + 10"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Este capítulo apresenta muitos tipos de expressões. Aprender a programar envolve experimentar tudo o que você aprende em combinação, investigando o comportamento do computador. O que acontece se você dividir por zero? O que acontece se você dividir duas vezes seguidas? Você nem sempre precisa perguntar a um especialista (ou à Internet); muitos desses detalhes podem ser descobertos experimentando-os você mesmo. "
   ]
  }
 ],
 "metadata": {
  "anaconda-cloud": {},
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.7.8"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
