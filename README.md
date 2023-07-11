# Hey! Let me explain you who's Daniel 😃

```python

"""
Hello there, dear visitor! 😃

Here's a quick walkthrough the 'source code' of my life:
    1. 'Person' - This class holds the simple truths of my being - my name, age, and location. The building blocks of identity, if you will.
    2. 'Developer' - Here's where it gets interesting. This class is the heart of my technical person, filled with the languages I speak, both human and machine, my education, my experiences, and more.
    3. 'Hobbyist' - Just as important as my professional life, this class holds the activities that bring me joy and relaxation in my downtime and make me feel complete.
    4. 'Me' - At the intersection of Person, Developer, and Hobbyist, 'Me' emerges. A synergy of all aspects of my life, it is an authentic representation of who I am.

And remember, 'Me' is a work in progress, ever-evolving, forever learning and mainly thanks to others. So stay tuned for more 'commits' and 'pushes' 🌱
"""

class Person:
    def __init__(self, name, age, location):
        self.name = name
        self.age = age
        self.location = location

    def introduce(self):
        return f"Hello! I'm {self.name}, {self.age} years old, living in {self.location}."

class Developer(Person):
    def __init__(self, name, age, location, languages, prog_languages, tools, libraries, frameworks, education, experience, projects):
        super().__init__(name, age, location)
        self.languages = languages
        self.prog_languages = prog_languages
        self.tools = tools
        self.libraries = libraries
        self.frameworks = frameworks
        self.education = education
        self.experience = experience
        self.projects = projects

    def introduce(self):
        introduction = super().introduce()
        return f"{introduction} I'm a Data Scientist and developer, graduated from {self.education}. "
    f"I work primarily with {', '.join(self.prog_languages)}, making use of tools like {', '.join(self.tools)}, "
    f"libraries such as {', '.join(self.libraries)}, and frameworks like {', '.join(self.frameworks)}. "
    f"I speak {', '.join(self.languages)}. My experiences include: {', '.join(self.experience)}. "
    f"Some of my significant projects are: {', '.join(self.projects)}."

class Hobbyist(Person):
    def __init__(self, name, age, location, hobbies):
        super().__init__(name, age, location)
        self.hobbies = hobbies

    def introduce(self):
        introduction = super().introduce()
        return f"{introduction} In my spare time, I enjoy {', '.join(self.hobbies)}."

class Me(Developer, Hobbyist):
    def __init__(self, name, age, location, languages, prog_languages, tools, libraries, frameworks, education, experience, projects, hobbies):
        Developer.__init__(self, name, age, location, languages, prog_languages, tools, libraries, frameworks, education, experience, projects)
        Hobbyist.__init__(self, name, age, location, hobbies)

    def introduce(self):
        introduction = super().introduce()
        return f"{introduction} Feel free to connect with me to learn more or collaborate on some exciting projects!"

if __name__ == "__main__":
    me = Me("Daniel Vahos", 23, "Paris", ["English", "French", "Spanish"], ["Python", "C", "C++"], ["Jupyter Notebook", "Google Colab"],
            ["Numpy", "Pandas", "Matplotlib", "Seaborn", "Sklearn", "Scipy"], ["TensorFlow", "PyTorch", "Keras"], "Télécom Paris",
            ["Data Science intern", "AI project Assistant", "IoT-mechatronics intern"],
            ["Feature Engineering", "Anomaly detection", "Deep Learning for Image Classification", "Time-Series Forecasting", "Data Mining", "Machine Learning in High Dimension"],
            ["Hanging out with friends", "Hiking", "Catholic Pilgrimages", "Psychology - Human behaviour", "Cinema"])
    print(me.introduce())
```
<!---
danielvahosm/danielvahosm is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
