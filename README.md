# Template de Trabalhos Acadêmicos da Universidade Estadual do Ceará 2025
Data de referência: Julho de 2025

# Sobre

Este modelo é uma alteração do modelo [**ueceTeX2**](https://github.com/thiagodnf/uecetex2).
A estrutura em si do projeto não foi alterada, apenas alguns ajustes foram feitos baseados na atualização do [Guia de Normalização Uece 2024](https://www.uece.br/biblioteca/wp-content/uploads/sites/27/2024/09/GUIA-UECE-2024-Atualizado-1.pdf).

## Alterações Realizadas 
  - Alteração no pontilhado do sumário, lista de figuras, lista de quadros, lista de ilustrações, lista de gráficos, etc;
  - Boa parte dos comentários foram apagados do código para que o aluno pouco habituado não se perca ou se assuste tanto (Coloquei eles ao final desse README);
  - As pré-configurações estão para alunos de licenciatura em matemática por padrão, mas podem ser alteradas sem dificuldade;
  - Alteração da Distância entre o O brasão da Uece e a margem superior da capa;
  - Alteração da Distância entre o nome do curso de graduação e o autor para 1,5cm. (Atente-se a centralização do título);
  - Alteração do nome Lista de Ilustrações para Lista de Figuras;
### Modelos Disponíveis
Os modelos disponíveis da versão 2019 continuam funcionando. 
Vale a ressalva de que as alterações foram realizadas apenas no que diz respeito ao TCC.
Casos particulares de modelos de Dissertação e Tese não foram observados.

**Trabalhos Acadêmicos**

 - Trabalho de Conclusão de Curso de Graduação
 - Trabalho de Conclusão de Curso de Especialização
 - Dissertação de Mestrado Acadêmico e Profissional
 - Tese de Doutorado
 
**Qualificações**

 - Qualificação para Mestrado Acadêmico e Profissional

# Por onde começo?
Para utilizar o ueceTeX2 você precisa seguir os seguintes passos:

1. Clique [aqui](https://github.com/thiagodnf/uecetex2/archive/master.zip) para baixar o projeto
2. Descompacte o arquivo no diretório onde vc deseja guardar os arquivos do seu trabalho
3. Crie o seu texto a partir do arquivo *documento.tex* distribuído no arquivo baixado. O arquivo possui comentários e é, em certa medida, auto-explicativo.

> Você é iniciante em LaTeX ou em abnTeX2? Clique [aqui](https://code.google.com/p/abntex2/wiki/PorOndeComecar) para acessar a página desenvolvida pela equipe do abnTeX2. Nesta página é possível acessar diversos links sobre o LaTeX e sobre o abnTeX2 como, por exemplo, a história do LaTeX e alguns minicursos desenvolvidos em outras universidades

# Como compilar?

Este modelo, assim como a versão de 2019, pode ser utilizado de várias maneiras. 
Aconselhamos que usuários inexperientes utilizem o [Overleaf](https://www.overleaf.com/) para a alteração.

$\textcolor{red}{OBSERVAÇÃO:}$ A depender do que será utilizado em seu trabalho, você pode ter problemas com tempo de compilação no Overleaf apresenta alguns problemas com tempo de compilação.
Isso pode ocorrer em textos com muitas figuras, principalmente aqueles que utilizam o tikz.

# Limitações
 Nenhuma limitação foi resolvida, então permanecem as limitações:
 
  - O modelo permite a participação de somente um co-orientador
  - A folha de aprovação da Dissertação suporta no máximo 5 pessoas (Orientador, Co-orientador e 3 membros externos)
  - A folha de aprovação da Tese suporta no máximo 6 pessoas (Orientador, Co-orientador e 4 membros externos)
  
# Dicas

Veja a seguir como inserir alguns elementos no seu texto.

### Como inserir uma Tabela
```tex
\begin{table}[h!]	
	\centering
	\Caption{\label{tab:label_da_tabela} Legenda da Tabela}
	\UECEtab{}{
		\begin{tabular}{ccll}
			\toprule
	    		Quisque & pharetra & tempus & vulputate \\
			\midrule \midrule
				E1 & Complete coverage & Both splice sites \\
				E2 & Complete coverage & Both splice sites \\
				E3 & Partial coverage & Both splice sites & Both \\
				E4 & Partial coverage & One splice site & Both \\
				E5 & Complete or coverage & No splice & Both \\
				E6 & No coverage & No splice sites\\
			\bottomrule
		\end{tabular}
	}{
		\Fonte{Elaborado pelo autor}
    }
\end{table}
```

### Como inserir um Quadro
```tex
\begin{quadro}[h!]	
	\centering
	\Caption{\label{qua:label_do_quadro} Legenda do Quadro}
	\UECEqua{}{
		\begin{tabular}{|c|c|}
			\hline
			Quisque & pharetra \\
			\hline
			E1 & Complete coverage  \\
			\hline
			E2 & Complete coverage \\
			\hline
		\end{tabular}
	}{
		\Fonte{Elaborado pelo autor}
	}
\end{quadro}
```

### Como inserir uma figura
```tex
\begin{figure}[h!]
	\centering
	\Caption{\label{fig:label_da_figura} Legenda da Figura}	
	\UECEfig{}{
	    \includegraphics[width=8cm]{figuras/figura-1}
	}{
	    \Fonte{Elaborado pelo autor}
	}	
\end{figure}
```

### Como inserir uma alínea
```tex
\begin{alineas}
	\item Lorem ipsum dolor sit amet;
    \item Praesent vitae nulla varius;
	\item Praesent quis erat eleifend;
	\item Mauris facilisis odio eu:
	\begin{subalineas}
		\item Integer non lacinia magna;
		\item Proin mattis placerat risus.
	\end{subalineas}
\end{alineas}
```

### Como criar Capítulos
```tex
\chapter{Fundamentação Teórica}
\label{cap:fundamentacao-teorica}
```

### Como criar Seções
```tex
% Seções Secundárias
\section{Objetivo Geral 2}
\label{sec:objetivo-geral-2}

% Seções Terciárias
\subsection{Objetivo Geral 3}
\label{sec:objetivo-geral-3}

% Seções Quaternárias
\subsubsection{Objetivo Geral 4}
\label{sec:objetivo-geral-4}

% Seções Quinárias
\subsubsubsection{Objetivo Geral 5}
\label{sec:objetivo-geral-5}
```

### Como inserir um algoritmo
```tex
\begin{algorithm}[h!]
	\SetSpacedAlgorithm
	\caption{\label{alg:algoritmo_de_colonica_de_formigas}Algoritmo de Otimização por Colônia de Formiga}
	\Entrada{Entrada do Algoritmo}
	\Saida{Saida do Algoritmo}
	\Inicio{
		Atribua os valores dos parâmetros\;
		Inicialize as trilhas de feromônios\;
		\Enqto{não atingir o critério de parada}{
			\Para{cada formiga}{
				Construa as Soluções\;
			}
			Aplique Busca Local (Opcional)\;
			Atualize o Feromônio\;
		}	
	}
\end{algorithm}
```

# Atenção
Assim como o UeceTeX2 de 2019, este modelo não é oficial da Uece (Não ainda).

# Agradecimentos
Meus sinceros agradecimentos aos desenvolvedores do UeceTeX2 que reduziram meu sofrimento em TCC, pois utilizei este modelo.

#### Links Úteis
[Por Onde Comecar](https://code.google.com/p/abntex2/wiki/PorOndeComecar)
[http://www.goes.uece.br](http://www.goes.uece.br)
[abnTeX2](https://code.google.com/p/abntex2/)
[Overleaf](https://www.overleaf.com/)

# Comentários Removidos

#### Comentários do document.tex
```tex
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%% Customizações do abnTeX2 (http://abnTeX2.googlecode.com)           %%
%% para a Universidade Estadual do Ceara - UECE                       %%
%%                                                                    %%
%% This work may be distributed and/or modified under the             %% 
%% conditions of the LaTeX Project Public License, either version 1.3 %%
%% of this license or (at your option) any later version.             %%
%% The latest version of this license is in                           %%
%%   http://www.latex-project.org/lppl.txt                            %%
%% and version 1.3 or later is part of all distributions of LaTeX     %%
%% version 2005/12/01 or later.                                       %%
%%                                                                    %%
%% This work has the LPPL maintenance status `maintained'.            %%
%%                                                                    %%
%% The Current Maintainer of this work is Thiago Nascimento           %%
%%                                                                    %%
%% Project available on: https://github.com/thiagodnf/uecetex2        %%
%%                                                                    %%
%% Further information about abnTeX2                                  %%
%% are available on http://abntex2.googlecode.com/                    %%
%%                                                                    %%
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%```

