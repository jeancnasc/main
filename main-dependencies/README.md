# Catálogo de artefatos

Este projeto cataloga os artefados usados pelos projetos, e controla as versões desses artefatos.

## Uso

Incluir na seção de gerenciamento de dependecias (dependencyManagement) do pom.xml do projeto, ou no pom.xml raiz no caso de projetos com multiplos módulos.

Exemplo:
```Xml
...
<dependencyManagement>
    <dependencies>
        <dependency>
            <groupId>io.github.jeancnasc.main</groupId>
            <artifactId>main-dependencies</artifactId>
            <version>1.0.0-SNAPSHOT</version>
            <type>pom</type>
            <scope>import</scope>
        </dependency>
    </dependencies>
</dependencyManagement>
...
```

Não incluir a versão dos artefatos que estão sendo gerenciados pelo main-dependecies.

Exemplo: A versão dos artefatos abaixo serão inferidas a partir do main-dependecies.
```Xml
...
<dependency>
    <groupId>io.github.jeancnasc.main</groupId>
    <artifactId>main-spring</artifactId>
</dependency>
<dependency>
    <groupId>io.github.jeancnasc.main</groupId>
    <artifactId>seguranca-spring</artifactId>
</dependency>

<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-web</artifactId>
</dependency>
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-data-jpa</artifactId>
</dependency>
...
```

## Adicionar nova biblioteca

Novas bibliotecas podem ser adicionadas a esse artefato sem a preocupação de afetar projetos já existentes, pois os artefados não são incluidos automáticamente aos projetos.

