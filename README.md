# Projeto de Banco de Dados I
Nome : Isadora Vitória do Rêgo Xavier <br/> 
Esse projeto consiste em um sistema de gerenciamento escolar utilizando o Modelo Entidade-Relacionamento. Sua realização foi baseada em vivências escolares, e implementado no program BrModelo. 

<img src="https://github.com/isadoravrx/banco_de_dados_1/blob/main/img_proj.png">

# Requisitos Mínimos
O projeto inicou-se com alguns requisitos mínimos, como:

- Criação de uma entidade Aluno, que possui alguns atributos como : Email, Telefone, notas, quantidade de faltas, sendo os três primeiros multivalorados, saldo da cantina, ID da matricula, que é uma chave para identificar o aluno. Atributos como série e turma também são inseridos, além do atributo derivado "turno".
- Entidade de professor, possuindo como atributo multivalorado as disciplinas ministradas por ele/ela, além do atributo "carteira de identificacao do professor", e possui relacionamento com aluno, já que o aluno é ensinado pelo professor, e relacionamento com disciplina, já que os professores são responsáveis por disciplinas.
- Entidade Disciplina, que possui como atributo seu nome, que serve como chave da entidade, e a sua carga horária. Além disso, possui relacionamento com as especificações de alunos, já que todos eles estudam disciplinas, e com a entidade "segmento", já que os segmentos do novo ensino médio são formados por disciplinas.
- Utilização de cardinalidade para representar a quantidade de entidades em cada relacionamento.
- especificações e generalizações, como "aluno", que pode ser EAD ou presencial, além da entidade "pessoa" que generalizou todos os indivíduos de um sistema escolar.

# Requisitos adicionais
Como Requisitos adicionais, foram inseridos: 

- A entidade "Pessoa" para generalizar todos aqueles indíviduos da escola, com o objetivo de agrupar os atributos que eles possuem em comum, que são : Nome(atributo composto, por primeiro nome e segundo nome),cpf, RG, dia, Mês e ano de nascimento, endereço, idade(atributo derivado da data de nascimento) e número da certidão de nascimento(chave da entidade).
- A entidade "Responsável financeiro", uma vez que em um sistem escolar, grande parte dos alunos são menores de idade e necessitam de um responsável. Caso Atingam a maior idade, podem ser seus próprios responsáveis financeiros, uma vez que a especificação de pessoa é do tipo sobreposição. Essa entidade possuirá como atributo uma conta bancaria, que servirá como chave da entidade. 
- Especificação da entidade "Aluno" em presencial e EAD, uma vez que uma grande quantidade de escolas vem se adequando a modalidade On-line. Na entidade "EAD", tem-se os atributos "usuário" e "senha", que serve como chave da entidade. Já na entidade "presencial", tem-se o atributo "senha catraca", que serve como chave da entidade, e representa a senha que o aluno deve colocar na catraca para entrar na escola.
- O atributo "saldo da cantina", na entidade "Aluno", uma vez que escolas vem cada vez mais reproduzindo um sistema financeiro interno, que permite que responsáveis coloquem saldo nas contas dos alunos, para comprarem alimentos na cantina.
- Entidade "Produtos_cantina" para representar tudo aquilo que é vendido na cantina, e "comprado" por "Aluno", como mostra o relacionamento "compra" entre "Aluno" e "produtos_cantina". Possui como atributos : "nome_produto", que é a chave da entidade, e "preco".
- Relacionamento "Possui como segmento novo ensino médio" entre as entidades "aluno" e "Segmento" para representar a nova mudança do ensino médio das escolas, que propõe cada aluno possuir um segmento. O atributo "nome do segmento" é chave dessa entidade. Como os seguimentos são compostos por disciplinas, tem-se também a relação "composto por" entre "segmento" e "disciplina".
- Entidade "Funcionário" que possui como atributo "nº do pis" e "conta bancária", documentação importante para contratação, e que servem como chave da entidade.
- Entidade "Funcionário" que possui especialização de sobreposição para as entidades "professor", "funcionário administrativo" e "funcionário da saúde".
- Entidade "professor", com o atributo "carteira_de_identificacao_do_professor"(chave da entidade), documento essencial dos professores.
- Entidade "funcionário administrativo" trabalham para departamentos, por isso o relacionamento, e servem para representar os funcionários administrativos dos departamentos da escola. Possui como atributo "registro cfa", documentação essencial para pessoas dessa área.
- Entidade "departamento", que possui como atributo chave o seu nome, e serve para representação dos departamentos que tem-se na escola.
- Entidade "Funcionário da saúde" para representar a parte da enfermaria da escola. Possui Relacionamento com "pessoa", já que eles os consultam. Possue o atributo "Profissão" para separação das funcões, e "registro do conselho regional". Esse atributos juntos, formam a chave da entidade, já que pessoas de diferentes profissões, podem ter o mesmo registro do seu específico conselho regional.
- Entidade "Transportador escolar", para representar os condutores que entram nas escolas para buscarem os alunos, por isso a relação entre essas duas entidades. Possuem como atributo : número da placa(que é a chave da entidade), responsável do veículo e quantidade de alunos(atributo derivado).
