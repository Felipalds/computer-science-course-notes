Change one thing for another in order to turns it illegible
Caesar cipher. Problem: the size of words is the same. And the letters are also encrypted the same way.
- Cyphertext-only attack. The above, knowing that the same letters appears
- Know-plaintext. If you discover one cipher, you can discover all.

Polyalphabetic cipher: the caesar cipher, but every position has a single unique shift.

PGP: secure e-mail
SSL: secure TCP
IPsec: secure IP


Hash vs Crypto
Crypto:
- gerar um valor a partir de uma chave. Essa chave deve ser compartilhada. Quem tiver a chave consegue ler o valor. 
- bidirecional
- AES, RSA
Hash:
- gerar uma impressão digital em um valor.
- unidirecional
- md5, sha1, sha256 (operações, XOR, OR, AND em blocos)
- gerados em CPU
- jamais gravar senha em plaintext
- não gravar senha encriptada no banco
- só gravar hash da senha é muito fraco (rainbow tables e dicionários)
- hash (salt + hash) já dificulta
- use argon2() bcrypt ou scrypt
- de tempos em tempos rehashear a senha
Base64: NÃO É ENCRIPTAÇÃO. É só converter binário para texto. Sem chave e sem nada!

RSA: Chaves públicas e privadas.


## Symetric Key Cryptography


## WEP - wired equivalency
1997 IEE 802.11
baixíssima segurança


1. dispositivo sem fio solicita autenticacao
2. o access point responde enviando um valor de 128 bytes, um nonce
3. o dispositivo entao encrypta usando a chave simétrica que foi compartilhada pelo access point
4. o access point decrypta o nonce 

## WPA - wifi protected
2003
melhoria temporária
mais seguro mas ainda muito vulneravel
TKIP (temporal key integrity protocol) e RC4
uso de AC

## WPA2
2004
obrigatório para todo dispositivo wifi
muito mais seguro
usa AES e CCMP
ataque KRACK (Key reinstalation attack)
handshake de 4 vias

## WPA3
versão mais atualizada
SAE (simultaneous auth of equals)
