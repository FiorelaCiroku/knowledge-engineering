# Ontology testing in XD 
This repository provides material and examples for the [Knowledge Engineering class](https://www.unibo.it/it/didattica/insegnamenti/insegnamento/2021/446613) class on ontology testing in eXtreme Design methodology, that will take place on December 14th.

## Video Tutorial and Slides

- [Video Tutorial](https://drive.google.com/file/d/1e59fchBLdbrzZgQWLiXhh8MFeeru1E6M/view?usp=sharing)
- [Slides](https://docs.google.com/presentation/d/1gzrQK8aqkAsdX72F7rbS9qAI94RuD0Uz/edit?usp=sharing&ouid=113864870076967859609&rtpof=true&sd=true)

## Links

-  [Carolina story](https://github.com/polifonia-project/stories/tree/main/Carolina:%20Music%20Historian)
-  [Musical performance ontology](https://github.com/polifonia-project/musical-performance-ontology)
-  [Core ontology](https://github.com/polifonia-project/core-ontology)
-  [OWLUnit GitHub repository](https://github.com/luigi-asprino/owl-unit)
-  [OWLUnit Releases](https://github.com/luigi-asprino/owl-unit/releases)
-  [TESTaLODE GitHub repository](https://github.com/TESTaLOD/TESTaLOD) 
-  [TESTaLODE website](http://testalod.herokuapp.com/)


## Assignment

### Sources

- Requirement for the competency question verification test: When was a recording produced?
- Ontologies that you need to use for the tests: [Musical performance ontology](https://github.com/polifonia-project/musical-performance-ontology) and [Core ontology](https://github.com/polifonia-project/core-ontology). 

<img width="600" alt="Screenshot 2021-12-10 at 02 46 04" src="https://user-images.githubusercontent.com/12375920/145503368-f8012afb-ca8f-471e-9174-386ff8e900b8.png">

### Tasks 

- Translate the competency question to a SPARQL query.
- Create a toy dataset for the competency question verification test based on the requirement.
- Create an expected result file for the competency question verification test based on the requirement.
- Construct a competency question verification test based on the requirement, including the above components.
- Create an inference verification test case on a requirement of your choosing.
- Create an error provocation test case. 
- Create a toy dataset for the error provocation test. 


### Competency question verification test

```turtle
@prefix owlunit: <https://w3id.org/OWLunit/ontology/> .

tc:xx a owlunit:CompetencyQuestionVerification ;
  owlunit:hasCompetencyQuestion " " ;
 	owlunit:hasSPARQLUnitTest " " ;
	owlunit:hasInputData td:xx ;
	owlunit:hasInputTestDataCategory owlunit:ToyDataset ;
	owlunit:hasExpectedResult " ";
	owlunit:testsOntology xx: .
```

### Inference verification test

```turtle
@prefix owlunit: <https://w3id.org/OWLunit/ontology/> . 

tc:xx a owlunit:InferenceVerification ;
	owlunit:hasInputData ex:xx ;
	owlunit:hasSPARQLUnitTest " " ;
	owlunit:hasReasoner owlunit:HermiT ;
	owlunit:hasExpectedResult true/false ;
 	owlunit:testsOntology xx: .
```

### Error provocation test

```turtle
@prefix owlunit: <https://w3id.org/OWLunit/ontology/> . 

tc:xx a owlunit:ErrorProvocation ;
	owlunit:hasInputData td:xx ;
 	owlunit:testsOntology xx: .

```
