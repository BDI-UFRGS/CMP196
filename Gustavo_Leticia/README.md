# Modelagem Ontológica do Sistema Petrolífero

## 1. Domínio

Um sistema petrolífero é um modelo conceitual fundamental para a exploração de hidrocarbonetos. Ele representa o conjunto de elementos geológicos e processos responsáveis pela geração, migração, aprisionamento e acumulação de petróleo e gás natural em bacias sedimentares. A modelagem conceitual utilizada para construir a representação desta pesquisa baseou-se nos conceitos abordados por Magoon e Dow (1994) .

Do ponto de vista geológico, o sistema petrolífero é composto por elementos essenciais, como rocha geradora, rocha reservatório, rocha selante e estruturas de armadilha, que interagem de forma interdependente ao longo do tempo geológico. A rocha geradora contém matéria orgânica que, submetida a condições específicas de temperatura e pressão decorrentes do soterramento sedimentar, passa pelo processo de geração de hidrocarbonetos. Os fluidos gerados são então expulsos e transportados por caminhos de migração, camadas permeáveis ou sistemas de falhas, em direção a zonas de menor pressão, caracterizando o processo de migração. Ao encontrar uma configuração geométrica favorável, os hidrocarbonetos se acumulam e formam depósitos, no processo denominado acumulação.

A diversidade terminológica entre disciplinas geocientíficas e formatos de dados da indústria, como RESQML e OSDU, criam desafios significativos de interoperabilidade semântica. A ontologia proposta, fundamentada na BFO e alinhada à GeoCore, fornece uma representação formal e processável por máquina dos conceitos do domínio, tornando explícito o significado das entidades, suas propriedades e relações. Isso viabiliza a integração de dados entre sistemas de modelagem de bacias e de reservatórios, a harmonização terminológica entre especialistas de diferentes disciplinas, e o suporte a inferências automáticas sobre o conhecimento do domínio.

## 2. Questões de Competência

As questões de competência abaixo orientaram o desenvolvimento da ontologia:

1. Quais entidades geológicas, substâncias, qualidades e processos constituem um sistema petrolífero?
2. Como as entidades e os processos geológicos interagem para possibilitar a geração, migração, aprisionamento e acumulação de hidrocarbonetos?
3. Quais propriedades e características geológicas influenciam a ocorrência e o comportamento dos hidrocarbonetos em um sistema petrolífero?
4. Como os componentes de um sistema petrolífero estão relacionados espacial e funcionalmente dentro de uma bacia sedimentar?
5. O que distingue as diferentes disposições relacionadas as corpos rochozos em um sistema petrolífero, como selo, geradoura e reservatório?
6. Como um sistema petrolífero pode ser formalmente representado em termos de entidades geológicas, qualidades, substâncias, processos e seus relacionamentos?



### 3.1 Continuantes Independentes

Entidades que existem de forma completa em qualquer instante de tempo e não dependem de outro portador para existir.

**Earth Fluid / Fluidos da Terra**

| Entidades   | Descrição                                                                                                                                                                              |
| ----------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Petroleum   | Um fluido terrestre que é uma ocorrência natural de hidrocarbonetos, seja em estado gasoso, líquido ou sólido, originada por processos termogênicos ou biogênicos na crosta terrestre. |
| Oil         | Um petróleo que se encontra em estado líquido a condições de superfície e é gerado principalmente por processos de maturação termal de matéria orgânica dentro da janela do óleo.      |
| Natural Gas | Um petróleo que se encontra em estado gasoso a condições de superfície e é gerado por processos termogênicos ou biogênicos.                                                            |

**Materiais Terrestres / Earth Material**

| Entidade         | Descrição                                                                                                                                                                                                   |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Organic Matter   | Um material terrestre que é composto por compostos de carbono de origem biológica, presente em rochas geradoras, e que sob condições específicas de temperatura e pressão se transforma em hidrocarbonetos. |
| Rock             | Um material terrestre que é um agregado natural de minerais e/ou matéria orgânica, cuja identidade é determinada por sua composição e origem.                                                               |
| Sedimentary Rock | Uma rocha que é formada pela deposição, compactação e cimentação de sedimentos ou precipitação química em ambientes superficiais ou subsuperficiais.                                                        |
| Igneous Rock     | Uma rocha que é formada pelo resfriamento e solidificação de magma, seja na superfície (extrusiva) ou em profundidade (intrusiva).                                                                          |
| Basalt           | Uma rocha ígnea que é de composição máfica e textura fina, originada pelo resfriamento rápido de lava vulcânica, comum em ambientes de rifte continental.                                                   |
| Limestone        | Uma rocha sedimentar que é composta predominantemente por carbonato de cálcio (calcita ou aragonita), de origem biogênica ou química, podendo atuar como reservatório ou selante.                           |
| Sandstone        | Uma rocha sedimentar que é composta por grãos de areia cimentados, caracterizada por porosidade e permeabilidade intergranulares que a tornam frequente candidata a reservatório.                           |
| Shale            | Uma rocha sedimentar que é de granulação fina, laminada, composta por partículas de argila e silte, frequentemente enriquecida em matéria orgânica, e associada às funções de rocha geradora e selante.     |

**Objetos Geológicos / GeologicalObject**

| Entidade           | Descrição                                                                                                                                                     |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Body of Rock       | Um objeto geológico que é um volume contínuo de rocha com extensão espacial definida, podendo corresponder a uma unidade litoestratigráfica.                  |
| Basin              | Um corpo rochoso que é uma depressão da crosta terrestre propícia ao acúmulo de sedimentos e à formação de sistemas petrolíferos.                             |
| Layer              | Um corpo rochoso que é uma camada ou estrato com propriedades relativamente homogêneas, delimitado por superfícies estratigráficas.                           |
| Shale Layer        | Uma camada que é constituída por folhelho.                                                                                                                    |
| Sandstone Layer    | Uma camada que é constituída por arenito.                                                                                                                     |
| Limestone Layer    | Uma camada que é constituída por calcário.                                                                                                                    |
| Dikes              | Um corpo rochoso que é um corpo ígneo tabular intrusivo, capaz de fornecer calor adicional à matéria orgânica adjacente ou de atuar como barreira de selagem. |
| Aggregate of Rocks | Um agregado de objetos que é composto por múltiplos corpos rochosos e que delimita geometricamente uma armadilha geológica.                                   |

**Estruturas Geológicas / GeologicalStructure**

| Entidade | Descrição                                                                                                                                                                                  |
| -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Trap     | Uma estrutura geológica que configura uma geometria tectônica ou estratigráfica, materializada em um ou mais corpos rochosos, capaz de promover o acúmulo e a retenção de hidrocarbonetos. |


### 3.2 Continuantes Dependentes

Entidades que dependem de um portador (*bearer*) para existir, sem existência independente.

#### Qualidades

| Entidade     | Descrição                                                                                                                                                                             | Portador     |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ |
| Porosity     | Uma qualidade que inere em um material rochoso e representa a proporção volumétrica de espaços vazios disponíveis para o armazenamento de fluidos.                                    | Rock, Layer  |
| Permeability | Uma qualidade que inere em um material rochoso e representa a capacidade de transmitir fluidos por meio de uma rede de poros interconectados.                                         | Rock         |
| Pressure     | Uma qualidade que inere em um corpo rochoso e representa a força exercida por unidade de área sobre seus constituintes, influenciando processos de geração e migração.                | Layer, Dikes |
| Temperature  | Uma qualidade que inere em um corpo rochoso e representa a medida da energia cinética média de suas partículas constituintes, determinando a janela de maturação da matéria orgânica. | Layer, Dikes |

#### Disposições

| Entidade  | Descrição                                                                                                                                                                                                 | Portador                         |
| --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------- |
| Source    | Uma disposição que inere em uma camada de rocha e, sob condições específicas de temperatura e pressão, confere a capacidade de gerar e expelir hidrocarbonetos a partir da matéria orgânica nela contida. | Shale Layer                      |
| Seal      | Uma disposição que inere em uma camada de rocha e confere a capacidade de impedir a migração de hidrocarbonetos por meio de baixa permeabilidade.                                                         | Shale Layer                      |
| Reservoir | Uma disposição que inere em uma camada de rocha e confere a capacidade de armazenar e transmitir fluidos por meio de sua porosidade e permeabilidade efetivas.                                            | Sandstone Layer, Limestone Layer |



### 3.3 Ocorrentes

Entidades que se desenvolvem no tempo e possuem partes temporais.

| Processo     | Descrição                                                                                                                                                               |
| ------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Generation   | Um processo que consiste na transformação da matéria orgânica em hidrocarbonetos sob a ação combinada de temperatura, pressão e tempo geológico em uma camada geradora. |
| Migration    | Um processo que consiste no transporte natural dos hidrocarbonetos desde a rocha geradora até uma armadilha geológica, por meio de caminhos permeáveis.                 |
| Accumulation | Um processo que consiste na concentração de hidrocarbonetos em uma armadilha geológica, resultando na formação de um depósito de petróleo e/ou gás.                     |



### 3.4 Relações

| Relação               | Semântica                                                                                            |
| --------------------- | ---------------------------------------------------------------------------------------------------- |
| contained_in          | Indica que o fluido hidrocarboneto está fisicamente contido em uma camada rochosa.                   |
| bounds                | Indica que um agregado de corpos rochosos delimita geometricamente uma armadilha.                    |
| high_concentration_of | Indica a concentração de matéria orgânica suficiente para caracterizar uma rocha geradora potencial. |
| constituted_by        | Indica a relação de constituição material entre uma camada e o tipo rochoso que a compõe.            |
| bearer_of             | Indica que uma camada rochosa é o portador de uma disposição funcional.                              |
| inheres_in            | Indica que uma qualidade (pressão, temperatura, porosidade, permeabilidade) inere em seu portador.   |
| has_participant       | Indica quais entidades participam de um processo geológico.                                          |
| precedes              | Expressa a ordem temporal entre geração → migração → acumulação.                                     |
| has_part              | Indica que uma armadilha é composta por camadas rochosas e/ou diques.                                |

## 5. Ontologias Importadas

| Ontologia    | URL de Importação                                                                      |
| ------------ | -------------------------------------------------------------------------------------- |
| **BFO 2020** | `http://purl.obolibrary.org/obo/bfo/2020/bfo.owl`                                      |
| **DUL**      | `http://www.ontologydesignpatterns.org/ont/dul/DUL.owl`                                |
| **GeoCore**  | `https://www.inf.ufrgs.br/bdi/ontologies/geocore/releases/2024-04-06/geocore-full.owl` |

---

# EN Ver.

# Ontological Modeling of the Petroleum System

## 1. Domain

A petroleum system is a fundamental conceptual model for hydrocarbon exploration. It represents the set of geological elements and processes responsible for the generation, migration, trapping, and accumulation of oil and natural gas in sedimentary basins. The conceptual modeling used to build the representation in this research is based on the concepts proposed by Magoon and Dow (1994).

From a geological perspective, a petroleum system is composed of essential elements such as source rock, reservoir rock, seal rock, and trap structures, which interact interdependently over geological time. The source rock contains organic matter which, under specific temperature and pressure conditions resulting from sedimentary burial, undergoes the process of hydrocarbon generation. The generated fluids are then expelled and transported through migration pathways, permeable layers, or fault systems toward zones of lower pressure, characterizing the migration process. Upon encountering a favorable geometric configuration, hydrocarbons accumulate and form deposits in a process known as accumulation.

Terminological diversity between geoscience disciplines and industry data formats, such as RESQML and OSDU, creates significant challenges for semantic interoperability. The proposed ontology, grounded in BFO and aligned with GeoCore, provides a formal and machine-processable representation of domain concepts, making explicit the meaning of entities, their properties, and relationships. This enables data integration between basin and reservoir modeling systems, harmonization of terminology across different disciplines, and support for automated inference over domain knowledge.

## 2. Competency Questions

The following competency questions guided the development of the ontology:

1. What geological entities, substances, qualities, and processes constitute a petroleum system?
2. How do geological entities and processes interact to enable the generation, migration, trapping, and accumulation of hydrocarbons?
3. What geological properties and characteristics influence the occurrence and behavior of hydrocarbons in a petroleum system?
4. How are the components of a petroleum system spatially and functionally related within a sedimentary basin?
5. What distinguishes the different dispositions associated with rock bodies in a petroleum system, such as seal, source, and reservoir?
6. How can a petroleum system be formally represented in terms of geological entities, qualities, substances, processes, and their relationships?

---

## 3.1 Independent Continuants

Entities that exist fully at any instant in time and do not depend on another bearer to exist.

### Earth Fluids

| Entities    | Description                                                                                                                                                                     |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Petroleum   | A terrestrial fluid consisting of naturally occurring hydrocarbons in gaseous, liquid, or solid state, originating from thermogenic or biogenic processes in the Earth’s crust. |
| Oil         | Petroleum in liquid state under surface conditions, mainly generated through thermal maturation of organic matter within the oil window.                                        |
| Natural Gas | Petroleum in gaseous state under surface conditions, generated through thermogenic or biogenic processes.                                                                       |

### Earth Materials

| Entity           | Description                                                                                                                                                                           |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Organic Matter   | Earth material composed of carbon-based compounds of biological origin, present in source rocks and transformed into hydrocarbons under specific temperature and pressure conditions. |
| Rock             | A terrestrial material consisting of a natural aggregate of minerals and/or organic matter, whose identity is determined by composition and origin.                                   |
| Sedimentary Rock | Rock formed by deposition, compaction, and cementation of sediments or by chemical precipitation in surface or subsurface environments.                                               |
| Igneous Rock     | Rock formed by cooling and solidification of magma, either at the surface (extrusive) or at depth (intrusive).                                                                        |
| Basalt           | An igneous rock of mafic composition and fine texture, formed by rapid cooling of volcanic lava, common in continental rift settings.                                                 |
| Limestone        | A sedimentary rock composed mainly of calcium carbonate (calcite or aragonite), of biogenic or chemical origin, and may act as reservoir or seal.                                     |
| Sandstone        | A sedimentary rock composed of cemented sand grains, characterized by intergranular porosity and permeability, making it a common reservoir candidate.                                |
| Shale            | A fine-grained, laminated sedimentary rock composed of clay and silt particles, often enriched in organic matter and associated with source and seal functions.                       |

### Geological Objects

| Entity             | Description                                                                                                                               |
| ------------------ | ----------------------------------------------------------------------------------------------------------------------------------------- |
| Body of Rock       | A geological object that is a continuous rock volume with defined spatial extent, potentially corresponding to a lithostratigraphic unit. |
| Basin              | A rock body representing a crustal depression favorable to sediment accumulation and petroleum system formation.                          |
| Layer              | A rock body that is a stratum with relatively homogeneous properties, bounded by stratigraphic surfaces.                                  |
| Shale Layer        | A layer composed of shale.                                                                                                                |
| Sandstone Layer    | A layer composed of sandstone.                                                                                                            |
| Limestone Layer    | A layer composed of limestone.                                                                                                            |
| Dikes              | A tabular intrusive igneous rock body capable of providing additional heat to adjacent organic matter or acting as a sealing barrier.     |
| Aggregate of Rocks | An aggregate composed of multiple rock bodies that geometrically defines a geological trap.                                               |

### Geological Structures

| Entity | Description                                                                                                                                                                |
| ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Trap   | A geological structure forming a tectonic or stratigraphic geometry, materialized in one or more rock bodies, capable of promoting hydrocarbon accumulation and retention. |

---

## 3.2 Dependent Continuants

Entities that depend on a bearer for their existence.

### Qualities

| Entity       | Description                                                                                                                 | Bearer       |
| ------------ | --------------------------------------------------------------------------------------------------------------------------- | ------------ |
| Porosity     | A quality inhering in a rock material representing the volumetric proportion of void spaces available for fluid storage.    | Rock, Layer  |
| Permeability | A quality inhering in a rock material representing its ability to transmit fluids through interconnected pore networks.     | Rock         |
| Pressure     | A quality inhering in a rock body representing force per unit area, influencing generation and migration processes.         | Layer, Dikes |
| Temperature  | A quality inhering in a rock body representing the average kinetic energy of its particles, controlling organic maturation. | Layer, Dikes |

### Dispositions

| Entity    | Description                                                                                                                                                                           | Bearer                           |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------- |
| Source    | A disposition inhering in a shale layer that, under specific temperature and pressure conditions, enables the generation and expulsion of hydrocarbons from contained organic matter. | Shale Layer                      |
| Seal      | A disposition inhering in a shale layer that prevents hydrocarbon migration due to low permeability.                                                                                  | Shale Layer                      |
| Reservoir | A disposition inhering in a rock layer that enables storage and transmission of fluids through effective porosity and permeability.                                                   | Sandstone Layer, Limestone Layer |

---

## 3.3 Occurrents

Entities that unfold in time and have temporal parts.

| Process      | Description                                                                                                                                      |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| Generation   | Process of transforming organic matter into hydrocarbons under combined effects of temperature, pressure, and geological time in a source layer. |
| Migration    | Process of natural transport of hydrocarbons from the source rock to a geological trap through permeable pathways.                               |
| Accumulation | Process of hydrocarbon concentration in a geological trap, resulting in the formation of an oil and/or gas deposit.                              |

---

## 3.4 Relations

| Relation              | Semantics                                                                                       |
| --------------------- | ----------------------------------------------------------------------------------------------- |
| contained_in          | Indicates that hydrocarbons are physically contained within a rock layer.                       |
| bounds                | Indicates that an aggregate of rock bodies geometrically defines a trap.                        |
| high_concentration_of | Indicates sufficient organic matter concentration to characterize a potential source rock.      |
| constituted_by        | Indicates material constitution between a layer and its rock type.                              |
| bearer_of             | Indicates that a rock layer is the bearer of a functional disposition.                          |
| inheres_in            | Indicates that a quality (pressure, temperature, porosity, permeability) inheres in its bearer. |
| has_participant       | Indicates which entities participate in a geological process.                                   |
| precedes              | Expresses temporal order between generation → migration → accumulation.                         |
| has_part              | Indicates that a trap is composed of rock layers and/or dikes.                                  |

---

## 5. Imported Ontologies

| Ontology     | Import URL                                                                                                                                                                   |
| ------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **BFO 2020** | [http://purl.obolibrary.org/obo/bfo/2020/bfo.owl](http://purl.obolibrary.org/obo/bfo/2020/bfo.owl)                                                                           |
| **DUL**      | [http://www.ontologydesignpatterns.org/ont/dul/DUL.owl](http://www.ontologydesignpatterns.org/ont/dul/DUL.owl)                                                               |
| **GeoCore**  | [https://www.inf.ufrgs.br/bdi/ontologies/geocore/releases/2024-04-06/geocore-full.owl](https://www.inf.ufrgs.br/bdi/ontologies/geocore/releases/2024-04-06/geocore-full.owl) |

