<h1 align="center">
   News_API
</h1>   

API de postagens de notícias criado em **Node.js** e **Express**. Em conjunto com <a href="https://github.com/Gilvan-R-A/News_System">News_System</a>, permite ao usuário cadastrar e visualizar postagens de notícias.   

## Requisitos   

- Git   
- Node instalado na sua máquina   
- Conhecimentos de Javascript e Node   

Para executar o projeto, digite o seguinte comando no seu terminal:   

``` javascript

node main.js   

```
  
<h3 align="center">
   Documentação da API
</h3>

  
## Método listarTodos( )


- **URL(Rota):**   
/postagem   
- **Método HTTP:**   
Get   
- **Parâmetros de URL:**   
Nenhum   
- **Parâmetro de Body:**   
Nenhum   
- **Resposta de Sucesso:**   
**Código:** 200 (OK)   

**Conteúdo:**   
```javascript
Postagem { 
“idpostagem”: valor,
 “titulopostagem”: valor,
 “conteudopostagem”: valor,
 “categoriapostagem”: valor,
 “datapostagem”: valor
 }   
 
 ```
- **Resposta de Erro:**   
**Código:** 404 (Não encontrado)   
**Conteúdo:** false
- **Exemplo de uso em JS:**   
```javascript   

var resposta = fetch(‘http://localhost:3000/postagem’);   

```   

## Método listarPorId( )   



- **URL (Rota):**   
/postagem/:idPostagem   
- **Método HTTP:**   
Get
- **Parâmetros de URL:**   
idPostagem   
- **Parâmetro de Body:**   
Nenhum   
- **Resposta de Sucesso:**   
**Código:** 200 (OK)   
**Conteúdo:**   
```javascript   

Postagem { 
“idpostagem”: valor,
 “titulopostagem”: valor,
 “conteudopostagem”: valor,
 “categoriapostagem”: valor,
 “datapostagem”: valor
 }   
 
 ```   
 
- **Resposta de Erro:**   
**Código:** 404 (Não encontrado)   
**Conteúdo:** false   
- **Exemplo de uso em JS:**   
```javascript   

var resposta = fetch(‘http://localhost:3000/postagem/1’);   

```   
 
## Método cadastrar( )


- **URL (Rota):**   
/postagem   
- **Método HTTP:**   
Post   
- **Parâmetros de URL:**   
Nenhum   
- **Parâmetro de Body:**   
```javascript   


Postagem: { 
 “titulopostagem”: valor,
 “conteudopostagem”: valor,
 “categoriapostagem”: valor,
 “datapostagem”: valor
 }   
 
 ```

- **Resposta de Sucesso:**   
**Código:** 201 (OK CRIADO)   
**Conteúdo:** true   
- **Resposta de Erro:**   
**Código:** 404 (Não encontrado)   
**Conteúdo:** false   
- **Exemplo de uso em JS:**   
```javascript   

var resposta = fetch(‘http://localhost:3000/postagem’, 
{
    method: 'post',
                headers: {
                    'Accept': 'application/json',
                    'Content-Type': 'application/json'
                },
                body: Objeto (Postagem)
 });   
   
   ```   
    
## Método alterar( )   


- **URL (Rota):**   
/postagem/:idPostagem   
- **Método HTTP:**   
Put   
- **Parâmetros de URL:**   
idPostagem   
- **Parâmetro de Body:**   
```javascript   

Postagem: { 
 “titulopostagem”: valor,
 “conteudopostagem”: valor,
 “categoriapostagem”: valor,
 “datapostagem”: valor
 }   
 
 ```   
 
- **Resposta de Sucesso:**   
**Código:** 200 (OK)   
**Conteúdo:** true   
- **Resposta de Erro:**   
**Código:** 404 (Não encontrado)   
**Conteúdo:** false   
- **Exemplo de uso em JS:**   
```javascript   

var resposta = fetch(‘http://localhost:3000/postagem/1’, 
{
    method: put,
                headers: {
                    'Accept': 'application/json',
                    'Content-Type': 'application/json'
                },
                body: Objeto (Postagem)
 });   
           
```   

            
## Método excluir( )   


- **URL (Rota):**   
/postagem/:idPostagem   
- **Método HTTP:**   
Delete   
- **Parâmetros de URL:**   
idPostagem   
- **Parâmetro de Body:**   
Nenhum   
- **Resposta de Sucesso:**   
**Código:** 200 (OK)   
**Conteúdo:** true   
- **Resposta de Erro:**   
**Código:** 404 (Não encontrado)   
**Conteúdo:** false   
- **Exemplo de uso em JS:**   
```javascript   

var resposta = fetch(‘http://localhost:3000/postagem/1’, {method: delete});   

```   
