# Basic and not-so-basic NumPy

## NumPy basics and not-so-basics

1. Work your way through the [NumPy arrays.ipynb notebook](../demos/Numpy%20arrays.ipynb) in the `demos` folder – at least the parts I didn't already cover.
2. Unless you are quite experienced with NumPy, work through this  great illustrated tutorial, testing the more challenging concepts as you go along: [NumPy Illustrated: The Visual Guide to NumPy (Lev Maximov)](https://betterprogramming.pub/3b1d4976de1d?sk=57b908a77aa44075a49293fa1631dd9b).
3. If/when you feel like it, try to do some of the [100 numpy exercises (with solutions)](https://github.com/rougier/numpy-100). Beware - they quickly get challenging! Be sure to think/try for a while before referring to the answer or hint that can be revealed by executing `hint(n)` or `answer(n)`.\
You can run them in as local environment by cloning or downloading the repository and then doing
    ```
    $ uv init
    $ uv add -r requirements.txt
    $ uv add ipykernel
    $ uv run python -m ipykernel install --user --name 'numpy-100'
    $ uv run --with jupyter jupyter lab
    ```  
    When you're finished with this, you can remove that kernel again using `uv run jupyter kernelspec remove numpy-100`.