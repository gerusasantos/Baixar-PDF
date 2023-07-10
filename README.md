import requests

def baixar_zip(url, destino):
    response = requests.get(url)
    with open(destino, 'wb') as arquivo:
        arquivo.write(response.content)
    print("Download concluído!")

# Exemplo de uso
url = "https://www.exemplo.com/arquivo.zip"
destino = "caminho/para/o/arquivo.zip"
baixar_zip(url, destino)
