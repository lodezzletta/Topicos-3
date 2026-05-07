# Laboratorio 1
Enzo Porto e Mello - 221006727

## Imagens
<img width="650" height="490" alt="Captura_de_tela_de_2026-05-06_21-21-44" src="https://github.com/user-attachments/assets/de60296d-cf33-43c7-af70-0053e9aa05f0" />
.
<img width="1092" height="980" alt="image" src="https://github.com/user-attachments/assets/89d1247e-065c-454d-9419-e9fa8452b374" />
.
<img width="1564" height="314" alt="2" src="https://github.com/user-attachments/assets/5e8b144c-2ff4-4fa5-9c5a-2bf57679a0af" />
.
<img width="830" height="185" alt="9" src="https://github.com/user-attachments/assets/75888c3f-8907-4d1f-8ff3-adebe463e463" />
.
<img width="830" height="185" alt="4" src="https://github.com/user-attachments/assets/7041e2a5-0c77-4ab1-9062-4e6bb5584118" />
.
<img width="830" height="185" alt="5" src="https://github.com/user-attachments/assets/43ffb084-3ce5-456e-8b57-13e2e634a7e2" />
.
<img width="830" height="185" alt="6" src="https://github.com/user-attachments/assets/cb8722cc-90f2-4970-94b7-c148b5ccd1a8" />
.
<img width="830" height="185" alt="7" src="https://github.com/user-attachments/assets/2a9581e0-4ce1-420a-a634-0a66dd73ef15" />
.
<img width="830" height="185" alt="8" src="https://github.com/user-attachments/assets/f77aece6-1a88-4a78-af63-4ff3b4cf988b" />

## Codigos
```bash
openssl enc -aes-256-ecb -salt -pbkdf2 -in texto.txt -out texto_ecb.enc
```
- ``` _openssl_ ``` chama o programa OpenSSL, que é uma ferramente de criptografia
-``` _enc_ ``` fala para o OpenSSL para usar a função de encryption, ou seja, decifrar ou cifrar arquivos.
    -``` _-d_``` seria para colocar no modo de decifrar, sem isso ele entende que é para criptografar.
- ```_-aes-256-ecb_```
    - ```_aes_``` algoritmo de criptografia.
    - ```_256_``` tamanho da chave, 256 bits.
    - ```_ecb_, _ctr_, _ofb_``` etc modos de operação.
- ```_-salt_``` é um valor aleatório usado junto com a senha para gerar a chave criptográfica, no qual evita que duas pessoas usando a mesma senha gerem exatamente a mesma chave.
-``` _-pbkdf2_ ``` faz o OpenSSL usar o método PBKDF2 para transformar sua senha em uma chave criptográfica.
    - Quando você digita uma senha, que nesse caso foi teste123, ela não é usada diretamente como chave AES. O OpenSSL precisa derivar uma chave de 256 bits a partir dessa senha, e o _-pbkdf2_ faz isso de forma mais segura.
- ```_-in texto.txt_ ``` define o arquivo de entrada.
- ```_-out texto_ecb.enc_``` define o arquivo de saída.
-```_diff_``` foi usado para comparar o arquivo original com o arquivo decifrado. Quando o comando não retorna nenhuma saída, isso indica que os dois arquivos são idênticos. Assim, foi possível confirmar que o processo de cifragem e decifragem funcionou corretamente.
- ```_time_``` mede quanto tempo um comando demora para executar.
    - ```_real_```  tempo total que passou no relógio.
    - ```_user_```  tempo gasto pelo processador executando o programa.
    - ```_sys_```   tempo gasto pelo sistema operacional.

## Perguntas
__Questão 1__ 

  O modo que apresentou o melhor desempenho na cifragem foi o OFB com tempo de 5,262 segundos.

__Questão 2__

  O ECB é inseguro pois ele criptografa blocos de texto idênticos em blocos de texto cifrado idênticos, ou seja, ele usa padrões reptidos para criptografar. Assim a estrutura dos dados podem ser revelados.

__Questão 3__

  Os modos mais adequados seriam o CTR, CFB e OFB, ja que permitem cifrar dados em sequência e geralmente os dados transmitidos na redes são transmitidos em partes.

__Questão 4__

  O Chacha20 cifra em fluxo de bits pseudoaleatorios. E o AES cifra em blocos de dados simétricos e se utiliza desses modos usados no laboratorio: ECB, CBC, CFB, OFB ou CTR.

__Questão 5__

  O Laboratorio mostra na prática como a criptografia simétrica é utilizada. E o TLS, IPsec e VPNs utilizam criptografias simétricas para proteger seus dados.


