# Relatório 1

## Descrição do Projeto - Atom

Atom é um editor de texto moderno, acessível. Além disso, é customizável ou capaz de ser usado de forma produtiva sem tocar num único ficheiro de configuração.

![Image](https://cdn-business.discourse.org/uploads/github_atom/490/d8548f4ce56f1599.png)

### Atom packages
  A nossa ideia é complementar um core package do Atom, [languague-html](https://atom.io/packages/language-html) (repositório do GitHub [aqui](https://github.com/atom/language-html)). Este package permite reconhecer linguagem HTML, fazer highlights da sintaxe da mesma, entre outras. Contudo, este não contém auto-close de tags html, sendo esta uma feature primária encontrada em outros editores da mesma gama (ex: Sublime Text Editor). Consideramos importante a implementação desta feature, pois permite uma programação mais produtiva.

## Processo de Desenvolvimento
  Desenvolvimento de software de código aberto (FLOSS - Free/Libre and Open Source Software)

  No círculo central encontram-se os "core developers" que contribuem com grande parte do código e supervisionam o design e evolução do projeto. No círculo a seguir deparamo-nos com os "co-developers". Estes são responsáveis pela submissão de patches, através de pull requests, como por exemplo correção de erros, os quais são revistos e aprovados pelos "core developers". Além disso existem ainda "active users", utilizadores ativos, cuja contribuição se baseia não em código mas sim em erros frequentes e aspetos a melhorar. Finalmente temos os "passive users", aqueles que se limitam a usar o programa sem emitir qualquer opinião ou crítica.



![Image](http://firstmonday.org/ojs/index.php/fm/article/viewFile/1207/1127/11449)

### Opiniões, Críticas e Alternativas

   Existem atualmente 1742 issues em aberto, estes preparados para todos os niveis de conhecimento de programação. Estes encontram-se rotulados com tags, como por exemplo, "beginner" que permite aos utilizadores menos experientes darem a sua contribuição entre outras como "help-wanted" para contruibuidores mais avançados.

   O Atom possui um ["Flight Manual"](http://flight-manual.atom.io/), que permite a qualquer developer a possibilidade de contribuir e de perceber facilmente a estrutura do atom.

   Este manual para além de explicar a estutura básica de funcionamento do Atom, como por exemplo que ficheiros de configuração lê quando se inicia, explica também como criar e modificar packages existentes.

   O facto de Atom estar organizado por packages facilita um desevnvolvimento constante das suas varias componentes sem requerer o lançamento constante de novas versões do mesmo. Por exemplo, se pretendermos adicionar funcionalidades ao suporte da linguagem HTML apenas temos que aceder ao package desta linguagem, o qual facilmente é distribuido para os restantes utilizadores, o que se tornaria bastante mais complexo e trabalhoso caso fosse necessario editar o Atom em completo por cada pequena melhoria.

   Esta divisão em packages permite ao Atom manter-se um editor de texto leve, dando a possibilidade ao utilizador de instalar apenas as extensões de acordo com as suas necessidades.

#### Alternativas

  Uma alternativa para desenvolvimento do Atom seria privatizar-lo e fechar-lo da comunidade open-source. Desta forma, seria possivel monetizar o mesmo, mas o numero de developers seria bastante reduzido levando a um crescimentos mais lento e fechado a novas ideias.

  Outra alternativa seria não estar organizado por packages, proporcionando uma distribuição mais pesada e levando a um lançamento mais lento e espaçado de novas versões.
