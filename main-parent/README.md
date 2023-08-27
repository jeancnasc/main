# Artefato Pai/Base dos projetos

Centraliza configurações padrões para os projetos, que incluem:

- geração do artejato sources.jar;

   Util para os desenvolvedores verem o código fonte de bibliotecas compartilhadas com mais facilidade.
 
  
- uso do main-dependecies;

  Projeto para centralização o versionamento de dependências.


- versão do java;

  Atualmente a versão 8

 
- incluir manifesto nos artefatos

  O manifesto contém dados sobre a geração do artefato, como a versão.

## Uso

Esse artefato deve ser usado como pai (parent) do projeto. 

```Xml
...
    <parent>
        <artifactId>main-parent</artifactId>
        <groupId>io.github.jeancnasc.main</groupId>
        <version>1.0.0-SNAPSHOT</version>
    </parent>
    
    <groupId>io.github.jeancnasc.main</groupId>
    <artifactId>template</artifactId>
    <version>1.0.0-SNAPSHOT</version>
...
```