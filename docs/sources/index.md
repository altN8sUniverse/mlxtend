
![](./img/logo_gray.png)

**A library consisting of useful tools and extensions for the day-to-day data science tasks.**

![Python 2.7](https://img.shields.io/badge/python-2.7-blue.svg)
![Python 3.4](https://img.shields.io/badge/python-3.4-blue.svg)
![License](https://img.shields.io/badge/license-BSD-blue.svg)

Sebastian Raschka 2014-2015

Current version: 0.2.6

<br>
<hr>

## Links
- Documentation: [http://rasbt.github.io/mlxtend/](http://rasbt.github.io/mlxtend/)
- Source code repository: [https://github.com/rasbt/mlxtend](https://github.com/rasbt/mlxtend)
- PyPI: [https://pypi.python.org/pypi/mlxtend](https://pypi.python.org/pypi/mlxtend)

<hr>
## Examples

	from mlxtend.evaluate import plot_decision_regions
	import matplotlib.pyplot as plt
	from sklearn import datasets
	from sklearn.svm import SVC

	# Loading some example data
	iris = datasets.load_iris()
	X = iris.data[:, [0,2]]
	y = iris.target

	# Training a classifier
	svm = SVC(C=0.5, kernel='linear')
	svm.fit(X,y)

	# Plotting decision regions
	plot_decision_regions(X, y, clf=svm, res=0.02, legend=2)

	# Adding axes annotations
	plt.xlabel('sepal length [cm]')
	plt.ylabel('petal length [cm]')
	plt.title('SVM on Iris')
	plt.show()</pre>

![](./docs/evaluate/img/evaluate_plot_decision_regions_2d.png)

