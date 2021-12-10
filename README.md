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

- Requirement for the competency question verification test: When was a recording produced?
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
