# Python Simple Progress Bar

A simple, easy-to-use progress bar for your time consuming operations in Python.

## Usage
````
bar = ProgressBar(100)
for i in range(0, 100):
    time.sleep(1)
    bar.update(i)
````
Output:

````
Progress: [##############      ] 70%
````

## Documentation
### Basics
You set the end value and update it at each iteration with the new value. Please note that it assumes values from 0 to `end_value`-1.

````
end_value = 63773
bar = ProgressBar(end_value)
for i in range(0, end_value):
    time.sleep(1)
    bar.update(i)
````

### Customization
#### Bar length
You can set the length of the bar (hashes) by setting `bar_length`. **Default:** 20.

````
bar = ProgressBar(100, bar_length=10)
for i in range(0, 100):
    time.sleep(1)
    bar.update(i)
````
````
Progress: [#######   ] 70%
````

#### Info Text
You can set the informative text before the bar by setting `text`. **Default:** `"Progress"`.

````
bar = ProgressBar(100, text="Iterations")
for i in range(0, 100):
    time.sleep(1)
    bar.update(i)
````
````
Iterations: [##############      ] 70%
````

## Compatibility
Compatible with Python 2 and 3.