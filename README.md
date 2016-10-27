To use this script, first run this to fit your first model:
    python kfkd.py fit
Then train a bunch of specialists that intiliaze their weights from
your first model:
    python kfkd.py fit_specialists net.pickle
Plot their error curves:
    python kfkd.py plot_learning_curves net-specialists.pickle
And finally make predictions to submit to Kaggle:
    python kfkd.py predict net-specialists.pickle

