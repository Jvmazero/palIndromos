import string

def eh_palindromo(texto):
    # Remover pontuações e espaços e converter para minúsculas
    translator = str.maketrans('', '', string.punctuation + ' ')
    texto_formatado = texto.translate(translator).lower()
    
    # Verificar se o texto formatado é igual ao seu reverso
    return texto_formatado == texto_formatado[::-1]

# Exemplo de texto para teste
texto_exemplo = "omissíssimo"

# Verificar se o texto exemplo é um palíndromo
if eh_palindromo(texto_exemplo):
    print(f'O texto "{texto_exemplo}" é um palíndromo!')
else:
    print(f'O texto "{texto_exemplo}" não é um palíndromo.')
