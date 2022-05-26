---
marp: true
theme: uncover
class: invert
title: Leaving the notebook
---

# Leaving the notebook

---
<!-- paginate: true -->
# Jupyter to Script

You can convert a jupyter notebook to a script with:

```bash
 $ jupyter nbconvert --to script [YOUR_NOTEBOOK].ipynb
```
You can even do this inside the notebook's cell with:
```py
!jupyter nbconvert --to script [YOUR_NOTEBOOK].ipynb 
```

---

# Ways to have your code in your path:
* Be in the same directory as your file (this is what we will do today)
* A subdirectory with ```__init__.py``` file. 
* Add the directory containing the file to your PATH
* Make your file into a package and install it (note: the book has a chapter on this)

--- 

# Command Line Invocation

```$ python3 [script].py ```
Invokes our script from the command line. 

By adding 

```py
if __name__ == '__main__':
    # Instructions for command line call go here
    # A useful pattern is sys.exit(main()) 
```

---

# Sidenote: Where do your tests go?
* 1-file projects:
    - In a file next to your code with a filename that starts with the word test
* Packages and modules:
    - Project level directory
        * code/src directory
        * tests directory