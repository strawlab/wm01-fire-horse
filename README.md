# wm01-fire-horse

## Introduction

This is the course material for WM-01: Bioinformatics, Summer Semester 2026
(year of the fire horse), Faculty of Biology, University of Freiburg. The
instructors are Prof. Dr. Andrew Straw, Dr. Michael Harrap and Dr. Wolfgang
Maier.

Links:
- main course repository [github](https://github.com/strawlab/wm01-fire-horse)
- ILIAS for exercise submission [ILIAS](https://ilias.uni-freiburg.de/ilias.php?baseClass=ilrepositorygui&ref_id=4289751)
- HisInOne for locations and times of lectures [HisInOne](https://campus.uni-freiburg.de/qisserver/pages/cm/exa/examEventOverviewOwn/showOverview.xhtml?_flowId=examEventOverviewOwn-flow&_flowExecutionKey=e2s3)
- HisInOne for locations and times of exercises [HisInOne](https://campus.uni-freiburg.de/qisserver/pages/cm/exa/examEventOverviewOwn/showOverview.xhtml?_flowId=examEventOverviewOwn-flow&_flowExecutionKey=e2s2)

The course is aimed at master's students in the biological sciences. Its goal is
 to develop computational thinking through practical programming and data
analysis. Python and Galaxy are the primary tools, but the emphasis is on
transferable ideas. Initially this is variables, loops, and functions. This then
moves to some use of the command line and working effectively with AI-assisted
(agentic) coding tools. Finally, Galaxy is used in the second half of the
course.

The course moves at a relatively fast pace appropriate for master students and
places less emphasis on Python syntax than on computational fluency.

No prior programming experience is assumed. The course moves quickly, however,
and students are expected to spend time practicing between lectures.

## Sunbeam application to run Jupyter Lab on your computer

[Sunbeam](https://github.com/strawlab/sunbeam) is software to make it easy to
install and run Python on your own laptop or other computer. If possible, please
perform the following test:

1) Download the latest version of Sunbeam from [releases](https://github.com/strawlab/sunbeam/releases)
2) Install it on your computer as a normal app.
- On macOS, because I have not paid for a developer license, there are another couple steps described here: https://github.com/strawlab/sunbeam#macos-allowing-an-unsigned-app-to-run
3) Start the Sunbeam program.
4) Click the "Launch Jupyter Lab" button in the Sunbeam window.
5) The first launch may take several minutes while Python and the required packages are downloaded.
6) A browser window should be opened running Jupyter on your machine

If you cannot launch Jupyter Lab before the first lecture, please bring your
laptop anyway and we'll help you get it working.

You can also use a PC in the computer pool.

## Python packages managed by `uv`

Sunbeam should, by default, install all packages needed. If you want to set them
manually, use [pyproject.toml](pyproject.toml).

## Useful resources

Python
* [The Python Tutor](http://pythontutor.com/)

AI assistants
* [openwebui.uni-freiburg.de](https://openwebui.uni-freiburg.de)
* [claude.ai](https://claude.ai)
* [ChatGPT](https://chatgpt.com)

## Lectures

| Lecture       | Summary                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| ------------- | -------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Lecture 1** | Course introduction, computational thinking, and Python basics | Introduction to the WM-01 course including format, grading, and teamwork policies. Computational thinking as the core transferable skill: decomposition, abstraction, and pattern recognition applied to biological problems. Deconstruction of Blockly programs to expose programming concepts without syntax overhead. Introduction to Jupyter notebooks and interactive Python. Fundamental concepts—built-in names, variables, assignment, functions, basic data types (`int`, `float`, `str`, `None`), and list indexing. The idea that programming is an iterative process of predicting, running, inspecting, and debugging. Framing the current reality that AI assistance is now part of software development while explaining why computational fundamentals remain essential. |
| **Lecture 2** | Programming fundamentals: control flow and data structures                 | A fast-paced continuation of core Python. Slicing and type coercion. Control flow with conditionals and `for`/`while` loops. Core data structures—lists, tuples, and dictionaries—and iteration over collections. Reading simple CSV files using the standard library. String formatting with f-strings. Good programming habits including readable code, avoiding repetition (DRY), and using small examples and `assert` statements to verify code. Emphasis throughout on concepts that transfer directly to shell scripting and scientific Python.                                                                                                         |
| **Lecture 3** | Command line, shell, and SSH                                               | Introduction to the Unix shell and remote computing using SSH. Connecting to a server, navigating the filesystem, editing files with `nano`, and viewing files with `cat` and `less`. Relative and absolute paths, environment variables such as `PATH`, and running Python programs from the command line. Command-line arguments via `sys.argv`, exit codes, and copying files with `scp`. Brief introduction to shell variables, loops, and pipes, reinforcing concepts from Lecture 2. Using AI assistants to compose, explain, and safely modify shell commands.                                                                                                                                          |
| **Lecture 4** | Agentic coding: working effectively with AI                                | How modern AI coding assistants work at a useful level of abstraction, including a brief introduction to transformers and large language models. Practical workflows for AI-assisted programming: decomposing problems, writing effective prompts, asking for explanations and tests, iteratively refining solutions, and debugging with AI. Reading, running, and *verifying* generated code rather than trusting it. Recognizing common failure modes including hallucinated APIs, plausible-but-wrong logic, and silent data errors. Reproducibility, provenance, and academic integrity when using AI. Applications both in Python and at the Unix command line.                                                    |
| **Lecture 5** | Data analysis and visualization with pandas and matplotlib                 | Introduction to pandas and the `DataFrame` abstraction for structured biological data. Loading, inspecting, filtering, grouping, and summarizing datasets. Creating publication-quality plots using matplotlib, including scatter plots, histograms, and line plots with appropriate labels and axes. Brief introduction to seaborn as a higher-level plotting interface. A pragmatic introduction to object-oriented ideas—objects, methods, and attributes—as needed to use scientific Python libraries fluently, without developing new classes.                                                                                                                                                                     |
| **Lecture 6** | Numerical computing and optimization with NumPy and SciPy                  | Introduction to NumPy as the foundation of scientific computing: arrays, shapes, dimensions, indexing, slicing, broadcasting, and vectorized computation. Comparison of vectorized array operations with explicit Python loops to motivate numerical computing. Numerical optimization with `scipy.optimize` to estimate parameters by minimizing objective functions. Worked biological example: parameterizing a bee trajectory and finding the point of closest approach to a flower. Establishes array thinking as the foundation for image analysis and machine learning.                                                                                                                                          |
| **Lecture 7** | Image analysis fundamentals                                                | Why computational image analysis matters in biology: throughput, reproducibility, and objective measurement. Images as NumPy arrays, pixel values, colour channels, dynamic range, and image file formats. Core concepts of image segmentation using thresholding, morphological operations (erosion and dilation), Gaussian filtering, background subtraction, and connected-component labeling. Practical demonstration using real biological video data to detect and measure moving objects.                                                                                                                                                                                                                        |
| **Lecture 8** | Machine learning for biological data                                       | Unsupervised learning with scikit-learn, including k-means clustering, Gaussian mixture models, and hierarchical clustering. Principal Component Analysis (PCA) for dimensionality reduction and visualization, illustrated using single-cell RNA-seq data. Introduction to neural networks: models, training, labelled data, and inference. Biological applications including DeepLabCut and YOLO for computer vision. Concluding discussion of embeddings, transformers, and large language models, connecting machine learning concepts back to the AI-assisted workflows introduced earlier in the course.                                                                                                          |


## Dates and assignments

Exercises are released daily. They should be completed on the same day and
submitted before the deadline.

| Exercise    | Due date (at 23:59) |
| ----------- | ------------------- |
| exercise-01 | 2026-07-06          |
| exercise-02 | 2026-07-07          |
| exercise-03 | 2026-07-08          |
| exercise-04 | 2026-07-09          |
| exercise-05 | 2026-07-10          |
| exercise-06 | 2026-07-13          |
| exercise-07 | 2026-07-14          |
| exercise-08 | 2026-07-15          |

Download assignments from the main course repository in the `exercises/release`
directory. Upload your daily assignments as .ipynb files directly into the
assignment folder in Ilias. **Do not change the file name from the original.**

## Repository layout

```
lectures/
    lecture-01/
        1 - Course Introduction.ipynb
        ...
    lecture-02/
        ...
exercises/
    release/
        exercise-01/
            1 - First Steps.ipynb
    source/
        exercise-01/
            1 - First Steps.ipynb
README.md
pyproject.toml
```

## Use of AI assistants

AI coding assistants are encouraged throughout this course.

However, your goal is not simply to produce working code. You are expected to understand, test, and be able to explain any code you submit. Generated code should always be verified before use.

Where required, exercises may ask you to document how AI tools were used.
