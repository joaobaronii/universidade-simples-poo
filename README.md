
# Sistema de Gerenciamento Acadêmico

Sistema de linha de comando desenvolvido em Java para gerenciamento de informações acadêmicas. Permite cadastrar estudantes (graduação e pós-graduação), professores, disciplinas, turmas e lançar notas. Usa arquivos texto para persistência de dados. Foi feito para a disciplina Programação Orientada a Objetos (3° período) do curso de Ciência da computação - UFU, tem como objetivo estudar conceitos básicos da programação orientada a objetos

## Funcionalidades

- Cadastro, visualização e remoção de estudantes
- Cadastro e gerenciamento de professores
- Criação, visualização e exclusão de turmas
- Associação de disciplinas às turmas
- Lançamento e visualização de notas
- Cálculo de média individual e por turma
- Persistência de dados em arquivos `.txt`



## Classes Principais

### `Main.java`
Classe principal com menus interativos para o usuário escolher entre ações relacionadas a estudantes, professores, turmas ou notas.

### `Estudante.java` (Classe base)
Contém dados comuns a todos os estudantes, como nome, CPF, data de nascimento e CRA.

#### Subclasses:
- **`Grad.java`**: Inclui informações adicionais sobre estágio e data de início do estágio.
- **`PostGrad.java`**: Inclui o tema da dissertação.

### `Professor.java`
Modela o professor, contendo nome, CPF, data de nascimento, início do contrato e departamento.

### `Disciplina.java`
Representa uma disciplina, com nome, código e carga horária.

### `Turma.java`
Contém uma lista de estudantes, o professor responsável, ano, semestre e a disciplina ministrada.

### `Notas.java`
Armazena as notas dos estudantes por turma. Permite calcular médias, atualizar e exibir notas.

### `TurmaNaoEncontrada.java`
Exceção personalizada usada quando uma turma não é encontrada.

### `ToTXT.java`
Interface utilizada para exportar dados de objetos em formato `.txt`.

## Arquivos de Dados

- `data.txt`: Armazena os dados das turmas, professores e estudantes.
- `dataNotas.txt`: Armazena as notas de cada estudante por turma.
