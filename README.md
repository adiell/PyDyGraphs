PyDyGraphs
-----
An interactive charting library using [Dygraphs](http://dygraphs.com/) embedded in the [Ipython Notebook](http://ipython.org/notebook.html).

## Intent

The [Ipython Notebook](http://ipython.org/notebook.html) is an excelent tool for interacting with python and displaying data in real time. While tools like [matplotlib](http://matplotlib.org/) can generate static plots in the [Ipython Notebook](http://ipython.org/notebook.html), interactive javascript plots are more desireable. This module can be readily included in an [Ipython Notebook](http://ipython.org/notebook.html) and then used to generate beautiful time series plots with [Dygraphs](http://dygraphs.com/).

## How It Works

This python module generates javascript that interacts with the [Dygraphs](http://dygraphs.com/) library, and passes it to the [Ipython Notebook](http://ipython.org/notebook.html) kernel for execution.

Currently the *PyDyGraphs* module depends on [Pandas](http://pandas.pydata.org/) to generate a JSON representation of the data for plotting. This required dependancy may be removed with future work. [Pandas](http://pandas.pydata.org/) can be installed via [pip](https://pypi.python.org/pypi/pip).

## Example

Running this code in an [Ipython Notebook](http://ipython.org/notebook.html) will generate a timeseries plot using the [Dygraphs](http://dygraphs.com/) javascript library.

    # Import pydygraphs and numpy
    import pydygraphs
    import numpy as np

    # Subplot example
    fig = pydygraphs.figure(width = 600, height = 400)

    # Form data for plot
    x = np.array(range(100))
    y = [np.sin(np.random.rand(100)),-np.sin(np.random.rand(100))]

    # Plot figure
    fig.plot(x,y, color=['navy','magenta'])
    fig.title("Figure 1")
    fig.xlabel('Series')
    fig.ylabel('Value')

    # Show figure:
    fig.show()

## Installation:
Simply clone this repository and include the *pydygraphs.py* module in your project.


