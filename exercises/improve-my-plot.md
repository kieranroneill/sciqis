# Improve my plot

_Practice_

Here is a fantastic plot I just made and plan to publish in a paper or thesis:

![Ansatz ladder plot with varied parameters](improve-my-plot-assets/ladder_ansatz.png)

Or is it – fantastic? Probably you can make it look cleaner, prettier and more informative. That's your task!

1. Find the plot, the data (stored as `.npy`), a notebook generating the plot above from the `.npy` file, and the script used to generate the raw data in the `improve-my-plots-assets` folder. You don't need to run the script (you can just plot from the stored data), but if you do want to run it, you need to install qcircsim in your environment with `uv add git+https://github.com/neago/sciqis-qcircsim-claude.git`.
2. Create an improved version of the plot. Give it some loving care! Make it as clear and informative as you can, and if you can also make it pretty, that's just a bonus.
3. Now come up with a completely different way of visualising the same data. This could be as an animation, an interactive ipywidget (see [Visualisation.ipynb](../demos/Visualisation.ipynb) as an example on how to do it), or maybe just an entirely different visual style. Feel free to expand on the data-generation script to e.g. plot a wider range of qubit and layer numbers.
4. When you're done with each of the improved visualisations, post it to the [#improved-plot](https://discord.com/channels/1527267313563205773/1534891628798414928) channel, along with a description of what thoughts you had about the design. If you've done an interactive widget or similar, you could perhaps record a screencast of how it works, or otherwise upload the notebook.
5. Optional: Ask your friendly neighbourhood AI to convert your plotting script from 2 and/or the original non-optimal script to Plotly and Bokeh. Does it look nicer? Is the syntax understandable? Would you like to try out those libraries in the future? [personally, I'm more than happy with matplotlib]