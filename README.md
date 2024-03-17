# Projeto de Banco de Dados I
Nome : Isadora Vitória do Rêgo Xavier
Esse projeto consiste em um sistema de gerenciamento escolar utilizando o Modelo Entidade-Relacionamento. Sua realização foi baseada em vivências escolares, e implementado no program BrModelo. 

# Requisitos Mínimos
O projeto inicou-se com alguns requisitos mínimos, como:

- Criação de uma entidade Aluno, que possui alguns atributos como : Email, Telefone, notas e quantidade de faltas, sendo os três primeiros multivalorados.
- Entidade de professor, possuindo como atributo multivalorado as disciplinas ministradas por ele/ela, e possui relacionamento com aluno, já que o aluno é ensinado pelo professor, e relacionamento com disciplina, já que os professores são responsáveis por disciplinas.
- Entidade Disciplina, que possui como atributo seu nome, e a sua carga horária. Além disso, possui relacionamento com as especificações de alunos, já que todos eles estudam disciplinas.
- Entidade Mátricula, que possui como atributo um ID, que é uma chave, para identificar o aluno. Atributos como série e turma também são inseridos, além do atributo derivado "turno".
- Utilização de cardinalidade para representar a quantidade de entidades em cada relacionamento.
- especificações e generalizações, como aluno, que pode ser EAD ou presencial.

# Requisitos adicionais
