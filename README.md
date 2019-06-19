# How to build your reading notes 

This summer we will be working together to build a machine learning knowledge base using Jupyter Notebook and Sphnix. 

Each student will be assigned a specific topic to research in, during which he or she will organize the research reports and corresponding code implementations into Jupyter Notebook files. Each topic will turn into a chapter in the knowledge base. 

We will be using [this](https://github.com/d2l-ai/d2l-zh) as a template. 

Below is a step-by-step guide on how to create and publish a new chapter to the knowledge base. 

1. Before we start, you may need to follow the steps below to install some packages

   ```
   pip install nbsphinx
   pip install recommonmark
   ```

2. clone the knowldge base from GitHub using

1. ```
   git clone git@github.com:JingyaXun/MAGICS_K19.git
   ```

2. create a new folder under ~/MAGICS_K19/build/ and save all your Jupyter Notebook files in there.

3. Under ~/MAGICS_K19/build/[your folder]/ create **index.md**. Your index.md should be in the following format. See ~/MAGICS_K19/sample_topic as an example.

   ```
   # [your topic]
   
   [Add topic intro here.] 
   
   ```eval_rst
   
   .. toctree::
      :maxdepth: 2
   
      # add all your jupyter notebooks here (ommit '.ipynb')
      notebook1
      notebook2
   /```
   ```

4. Open ~/MAGICS_K19/build/index.rst and add the following text to the end of the file

   ```
   [your folder]/index
   ```

5. Under ~/MAGICS_K19/build/ execute the following command in your terminal

   ```
   make html
   ```

6. Next navigate to ~/MAGICS_K19/build/_build/html and click open **index.html**

7. Now you should be able to see your topic in the knowledge base and your Jupyter Notebook files can be viewed within that topic