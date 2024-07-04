# qcrusher-beta

Q-Crusher is a community-driven practice question tool. There are many ways to study for an exam, but there are not that many platforms where you can try some practice questions. 

Warning:

- Questions should not be copied from real exams (also not based on real exam questions).
- Questions should not be copied from copyright material, such as other training platforms.

## Categories

Currently the project structure and website structure is:

- Cloud
  - AWS
    - Cloud Practitioner
      - Pre-test
      - Practice Set 1
      - Official Sample Questions

This could be extended for example to 

- Cloud / Terraform / Associate / Name of the set
- Cloud / Azure / AZ-900 / Name of the set
- Programming / Python / Beginner / Name of the set
- Etc

## Add a question

Use this template:

```text
{{%/* question */%}}
question: |
    Question here
explanation: |
    Explanation here
answers:
    - answer: ""
      correct: True
    - answer: ""
    - answer: ""
    - answer: ""
{{%/* /question */%}}
```

And an example:

```text
{{%/* question */%}}
question: |
    Which is not a planet?
explanation: |
    Pluto is not a planet anymore. [Check this news](https://www.britannica.com/story/why-is-pluto-no-longer-a-planet)
answers:
    - answer: "Pluto"
      correct: True
    - answer: "Jupiter"
    - answer: "Mars"
    - answer: "Earth"
{{%/* /question */%}}
```

Two optional settings:

- `shuffle_answers: False`. Default: `True`. Will shuffle the answers randomly for you. In case you use A, B, C, D in the answers and the explanation, it's recommended to turn shuffle answers off.
- `answer_validation: False`. Default: `True`. Before checking your answers, it first validates if you checked the exact number of correct answers. Sometimes questions are too easy when it warns there are x answers correct. For example in a question with 4 answers and 3 answers are correct.

