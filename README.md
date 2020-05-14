# A quick start guide to Python and Github

Let me start by saying that Python is an amazing tool for literally *anyone* to know, but this is especially true for neuroscientists of all kinds. Python is a general-purpose programming language, meaning that it was designed to be flexible enough to be used for writing software for nearly any task, from signal processing to statistics to web scraping. Because there are nearly infinite ways to use Python, there are also many ways to install and use Python which can making getting started a daunting task for beginners. This was written to be a guide for going from zero Python (or any programming) knowledge to up-and-running as quickly as possible with the goal of data science in mind.

That being said, this guide is built around what I have found to be the best for getting started and many of my personal preferences. This is far from an end-all and once you are more familiar you may want to experiment with other IDEs and/or workflows to see what suits you best.

## Getting started with Python

### What is Python and why should you use it?

As mentioned above, Python is a **general-purpose programming language** which means that it was designed to be used for writing software of wide varieties. Although programming languages such as Python or MATLAB may be required for some scientific problems, such as digital signal processing, many problems can be solved by using simpler software such as Excel. However, Excel requires manual data curation which is **slow**, prone to **user-error**, and is often **difficult to reproduce** (even by the original user). In contrast, with Python you can _*speed up*_ your workflow by automating what you would normally do by hand in Excel, which in turn will _*decrease*_ user-error and _*increase*_ reproducibility --- all of which scientists should strive for.

You may be thinking "Yes, but I already know how to do everything in Excel and I don't have the time to learn all of this now." It's true that one of the problems stopping people from learning programming languages is that languages often have a steep learning curve, which is why I'm writing to speed this process up, but more importantly, improving your existing workflow is not the only benefit from learning to code! Knowing how to program is a skill like any other and having that skill will allow you to solve problems that you previously thought impossible (or at least not worth the time) and open doors that you never knew existed --- especially using a general-purpose language such as Python. Moreover, programming in Python has become a highly sought-after, and even required, skill in many industries (including academia) which means that learning it is particularly important for younger scientists.

> TL;DR -- Python speeds up workflows, allows for new/improved problem solving, and is critical to learn for young scientists

### How to download/install Python

One of the hardest parts of beginning with Python is trying to figure out what all you need to install. Python was originally developed with a core set of basic functions but since then many packages of Python functions (plotting, statistics, signal processing, etc.) have been developed independently, and all of these packages must be installed individually. Thankfully, the [Anaconda distribution](https://www.anaconda.com/products/individual) is here to solve this problem. Anaconda is a distribution of packages and software with data science in mind. So, instead of having to install a million different packages and software, we only need to install Anaconda, which includes:

* Python and R
* package managers for installing new packages (pip and conda)
* Many core packages needed for data science (NumPy, Pandas, SciPy, matplotlib)
* IDEs (Jupyter, Spyder, RStudio)

You should pick the latest version of Python 3 in 64-bit.

> TL;DR -- Install the 64-bit version of [Anaconda](https://www.anaconda.com/products/individual) with Python 3

### How to start using Python

Now that you have installed Anaconda you can start programming in Python using which ever integrated development environment (IDE) that you wish (or you also program directly in the the terminal, but this would be overcomplicated for beginners). IDEs combine editing, execution, plotting, debugging, and other functionalities into a single package, and thus make writing and executing code a breeze. There are a number of good IDEs out there for Python (Jupyter, Spyder, VSCode, PyCharm, etc.) but I highly recommend starting with [Jupyter](https://jupyter.org/) (specifically, Jupyter Notebooks). Jupyter is an easy-to-use IDE that just focuses on writing code without having to worry about advanced programming tools such a debuggers, variable inspectors, or consoles.

As the name suggests, Jupyter Notebooks combines running sections of code with  [Markdown](https://commonmark.org/help/) text formatting to create a notebook-like environment. This is great for documenting your scripts and creating templates and tutorials. Indeed, many example scripts and tutorials are written in Jupyter (.ipynb files), so understanding how to use Jupyter will go a long way to speed up the learning process.

> tl;dr -- From the Anaconda Navigator, launch Jupyter Notebook

### How to code with Python (syntax)

*I've section kept this brief. There are many excellent tutorials out there for practicing code --- this section is merely meant to introduce you to the most basic functionality and importing packages*

Now that you have Jupyter open you can start coding. To open a notebook, go to a directory where you want you notebook (.ipynb file) to live and click New -> Python 3. As per tradition, let's start creating your very first variable and see how output works in Jupyter! To practice the above code, you can copy and paste or hand type it. I highly recommend hand-typing and playing around with this code to see how it works! The only way to get better at coding is by coding!

```Python
my_first_variable = 'Hello world'
print(my_first_variable)
```

In the above cell, the *string* 'Hello world' is saved as the variable **my_first_variable**. This string can then be output or displayed by using the print() function and inputing **my_first_variable**.

Now let's import some fun packages to play around with numbers: Numpy and Pandas.

To import packages:

```Python
import numpy as np
import pandas as pd
```

Create a matrix of data:
```Python
data = np.array([[1,2,3],[4,5,6],[7,8,9]])
print(data)
```

Create a dataframe:
```Python
my_dataframe = pd.DataFrame(data, columns=['a', 'b', 'c'])
print(my_dataframe)
```

Index individual columns of your dataframe:
```Python
print(my_dataframe.a)
print(my_dataframe.b)
print(my_dataframe.c)
```

With the above code we can see how numpy allows us to create arrays and matrixes of data, and then pandas can take those matrixes along with metadata (column names) to create ways to precisely index data within a dataframe. This is a particularly powerful tool which comes in handy for plotting and running statistical analyses on specific data.

Below are more sources for learning Python. I cannot recommend the Python BootCamp by the Allen Institute enough. Download the notebooks and go through them. *Don't just read over them and feel like you learned something.* I can't stress enough that you have to actually code to learn it. The more time you invest in the beginning, the more time you save in the long run.

* [Python BootCamp from the Allen Institute](https://github.com/AllenInstitute/SWDB_2019)
* [15 Free Courses to Learn Python in 2020](https://medium.com/swlh/5-free-python-courses-for-beginners-to-learn-online-e1ca90687caf)
* *More soon*

> there is no tl;dr for this section - go back, read, code!

### How to install other Python packages

Now you should be up and running with Python and can begin playing around with the basics. As perviously mentioned, Anaconda comes with many important data science packages such as [NumPy](https://numpy.org/) arrays for working with numbers, [Pandas](https://pandas.pydata.org/) dataframes for manipulating and analyzing data, [SciPy](https://www.scipy.org/) for a wide variety of scientific computing tools, and [matplotlib](https://matplotlib.org/) for plotting and visualization. However, there are *many* packages that do not come with Anaconda, and new useful packages are constantly being created. Thankfully, most packages can be installed with the package manager, pip, which is as simple as typing ```pip install desired-package``` into the terminal.

For an example, you can try installing two of my personal favorite packages: [Pingouin](https://pingouin-stats.org/index.html) for easy-to-use statistical testing, and [Seaborn](https://seaborn.pydata.org/index.html) for better statistical plotting. If you go to their homepages you will find installation instructions as simple as:

    pip install seaborn

and

    pip install pingouin

To install, just open your terminal, code and paste the above code, and hit enter. That's it! Some packages may not be able to be installed via pip, but all packages usually still include very simple instructions for how to install.

> tl;dr -- in the terminal: ```pip install desired-package```

5. Final advice: find a project and work on it everyday

TODO


#### Other resources

[A Beginner's Guide to Python for Data Science](https://towardsdatascience.com/a-beginners-guide-to-python-for-data-science-60ef022b7b67)

^ This article summarizes an efficient way to get started:
1. Python basics: Install using Anaconda and recommends learning resources
2. Lists and Strings: understand list and strings
3. Python Libraries for Data Science: Jupyter notebook, NumPy, Pandas, Matplotlib, Scipy, PyTorch, scikit-learning
4. Pracitce Your Coding and Data Science Skills: Kaggle, Create and solve problems, take courses

---

## Getting started with GitHub

> SOON

1. What is Github and why should you use it?
2. How to download/install Github
2. How to get started with Github
3. Using the terminal is confusing, can I not?
