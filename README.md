# Boas práticas de programação e trabalho em equipe: exemplos de um sistema de gestão de faculdade

A qualidade do código tem influência direta na compreensão, manutenção e evolução de um sistema. Na fase de desenvolvimento, desenvolvedores diferentes de uma equipe podem trabalhar na correção de erros e adicionar novas funcionalidades num projeto. Assim, é importante garantir código organizado para facilitar o trabalho em equipe. Isso também ajuda a reduzir o tempo para entender como uma aplicação funciona.

Por exemplo, foi desenvolvido um sistema de gestão de faculdade na atividade em squad do Módulo 5 deste bootcamp. O objetivo principal era praticar os conceitos de POO com C#. Um exemplo de boas práticas dessa atividade é o uso de nomes significativos como os métodos `MatricularAlunoCurso` e `RegistrarNota` que demonstram a ação a ser realizada. Propriedades como `NumeroMatricula` e `ProfessorResponsavel` facilitam a identificação dos dados. Isto melhora a legibilidade do código e faz com quem comece a trabalhar no projeto consiga compreender as operações com o menor esforço possível.

Outra prática importante é a reutilização de código. No gerenciador de faculdade, as classes `Aluno` e `Professor` herdam da classe `Pessoa` pois ela agrupa informações em comum como `Nome`, `CPF` e `e-mail`. Isto evita repetir implementações iguais nas duas classes como as validações.

Por outro lado, por ser uma atividade para praticar conceitos de POO, a separação pode ser melhorada. A classe `FaculdadeService`, por exemplo, possui diversas operações e apresenta as informações diretamente no console. Uma melhoria possível seria separar a exibição dos resultados nas regras de negócio. Assim, ficaria mais fácil reutilizar as operações numa interface web. Se o sistema crescer, seria necessário avaliar a divisão da classe `FaculdadeService` em serviços com responsabilidades mais específicas.

Outro ponto a ser considerado é a padronização. No projeto, o menu chama o método `VincularDisciplinaCurso` enquanto o serviço utiliza `VincularDisciplinaAoCurso`. Embora expressem algo semelhante, a pequena diferença impede que a chamada encontre o método definido e cause erro de compilação. Logo, combinar nomes e parâmetros, revisar alterações e verificar se tudo funciona em conjunto é de extrema importância, e faz parte da comunicação em equipe.

Além dos pontos mencionados, o projeto pode incluir outras melhorias, como corrigir a inicialização da lista de disciplinas na classe `Curso` e proteger as coleções contra alterações diretas, garantindo que as modificações passem pelos métodos responsáveis pelas validações. Também seria importante centralizar regras para evitar validações duplicadas e melhorar o tratamento de entradas inválidas com mensagens claras para o usuário.

Entre os benefícios das práticas mencionadas estão a facilidade de manutenção e colaboração em equipe. Um código legível ajuda a localizar erros e realizar alterações com segurança. A padronização reduz dúvidas durante a entrega de novas funcionalidades. Tudo isso evita retrabalho, regras duplicadas e dificuldade para adicionar recursos novos.

Em resumo, desenvolver código exige atenção à clareza, consistência e organização de suas partes. O sistema de gestão de faculdade demonstra que boas práticas podem ser aplicadas até em projetos pequenos.

## Referência

Projeto utilizado como exemplo: [Sistema de Gestão de Faculdade](https://github.com/juliana-matias-it/sistema-de-gestao-de-faculdade).
