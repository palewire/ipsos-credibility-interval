# ipsos-credibility-intervals

A Python tool that calculates Bayesian credibility intervals for online polling using the Ipsos method

The Ipsos credibility interval is a Bayesian metric that can be used to calculate the margin of error for online polling. It estimates accuracy plus or minus a number of percentage points. You can learn more by reading [the Ipsos white paper](https://www.ipsos.com/sites/default/files/2017-03/IpsosPA_CredibilityIntervals.pdf).

## Installation

```bash
pip install ipsos-credibility-intervals
```

## Usage

Import the library and provide the sample size. The function will return the credibility interval in percentage points.

```python
import ipsos_credibility_intervals as ici

ici.get(1000)
3.5333753221609374
```

You can provide a custom confidence level. The default is 95%. This would return the interval for a 99% confidence level:

```python
ici.get(1000, confidence_level=0.99)
```

You can also customize the weighting factor designed by Ipsos The default is 1.3. This would return the interval for a weighting factor of 1.5:

```python
ici.get(1000, weight=1.5)
3.7954539356449795
```

## Other resources

- [The Ipsos white paper](https://www.ipsos.com/sites/default/files/2017-03/IpsosPA_CredibilityIntervals.pdf)
- [Code repository](https://github.com/palewire/ipsos-credibility-interval)
- [PyPI package](https://pypi.org/project/ipsos-credibility-intervals/)
