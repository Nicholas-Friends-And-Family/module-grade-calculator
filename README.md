# Module Grade Calculator

A small Java program designed to help you work out your current grade in a module. You just enter your marks for assignments, exams, or other assessments, and it will calculate your overall grade so you can see how you’re doing.

## Prerequisites 📋

- Should know how to open and use a [terminal](https://en.wikipedia.org/wiki/Computer_terminal).
- Basic understanding of [Git](https://git-scm.com/) & [JSON](https://www.json.org/json-en.html).

## Installation 🛠️

1. Click the green "Code" button and copy the url.

<img width="505" height="383" alt="image" src="https://github.com/user-attachments/assets/d064b539-b1f6-49e0-b541-b9ad946c66a1" />


2. Clone the project in your desired location.

```
$ git clone https://github.com/alsonick/module-grade-calculator.git
```

3. Open the project in your preferred IDE or code editor.

## Data 💾

You don't need to modify the source code, all you need to do is input your data into `data.json`

Here's how the JSON structure should look like:

> This alone won't compile properly, you need to fill the fields with your own data.

```json
{
  "modules": [
    {
      "name": "",
      "stage": 0,
      "coursework": [
        {
          "component": "",
          "title": "",
          "type": "",
          "mark": 0
        }
      ]
    }
  ]
}
```

> All the fields should be self explanatory but there might be some confusion with the `component`field, the component field is basically the _weight_ amount of the assignment or exam.

If you'd like to only test it with some dummy data (my actual grades) then copy this into the `data.json` file.

```json
{
  "modules": [
    {
      "name": "Databases and the Web",
      "stage": 1,
      "coursework": [
        {
          "title": "A1 - HTML & Javascript",
          "type": "Coursework",
          "component": 25,
          "mark": 89
        },
        {
          "title": "A2 - Databases & PHP",
          "type": "Coursework",
          "component": 25,
          "mark": 95
        },
        {
          "title": "Exam",
          "type": "Coursework",
          "component": 50,
          "mark": 70
        }
      ]
    }
  ]
}
```

> The `type` field should either be 'Assignment', 'Test', 'Coursework' or 'Examination', if neither of these types are provided, then 'Invalid' will be set as the type.

## Running ▶️

Run the `ModuleGradeCalculator` class and you should see the result printed in the terminal.

Here's an example response:

```
--------------------

Databases and the Web | Stage: 1 | Grade Summary:

Coursework: A1 - HTML & Javascript, Mark = 89, Component = 25%
Coursework: A2 - Databases & PHP, Mark = 95, Component = 25%
Coursework: Exam, Mark = 70, Component = 50%

Final Grade: 81.00

--------------------
```

![ScreenRecording2025-09-09at14 55 24-ezgif com-optimize](https://github.com/user-attachments/assets/ea4e30d8-510c-48fc-914e-120ebc7bd4e3)

## License 📜

MIT License
