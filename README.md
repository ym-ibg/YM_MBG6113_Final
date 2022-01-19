# YM_MBG6113_Final
All steps given here were done in *jupyter notebook* which was downloaded using [*Anaconda Navigator*](https://docs.anaconda.com/anaconda/install/windows/). Then, *numpy* and *matplot* were imported as they are required to achieve the assignments given in the [Final Exam.docx](https://github.com/ym-ibg/YM_MBG6113_Final/raw/main/Final%20Exam.docx).

<pre><code>import numpy as np
import matplotlib.pylab as plt
</pre></code>

## Q1.1
A two dimentional 100x100 array including rondom numbers between 0 and 100 was formed. To be able to create random numbers *rondom* function was imported. Then the array *ym100* was created.
<pre><code>from numpy import random
ym100 = random.randint (100, size=(100,100))
print(ym100)
</pre></code>
The output is given below:

![image](https://user-images.githubusercontent.com/95583564/150120126-0a9e21c1-d6a2-4ce7-b980-9df90c446a15.png)

## Q1.2 

A heatmap was created using the values in *ym100* and a colorbar was added to show color scales. The heatmap was saved as *ym100_heatmap.png* with an image quality of 600 dpi.

<pre><code>plt.imshow(ym100, cmap='hot', interpolation='nearest')
plt.colorbar()
plt.savefig('ym100_heatmap.png', dpi=600)
plt.show()</pre></code>

The resulting heatmap:

![ym100_heatmap](https://user-images.githubusercontent.com/95583564/150121256-43023411-7c11-4c3a-8aa8-8265bbd6f87a.png)

## Q2.1

Odd and even numbers in the matrix *ym100* was depicted and indexed into another matrix *ym_odds_evens*. The resulting matrix is composed of two statements *True* and *False* based on the number in the relative coordinate is even or odd, respectively.

<pre><code> ym_odds_evens = (ym100 %2 == 0)
print(ym_odds_evens) </pre></code>

The output:

![image](https://user-images.githubusercontent.com/95583564/150122170-dd5b72dd-4e90-42bb-bf83-f80f0dfe627f.png)

To make the matrix more readable the statements in ym_odds_evens were changed into 1 (true; even) and 0 (false; odd) by multiplying the matrix by 1 and indexing the result into another matrix called *ym_01*.


<pre><code>ym_01 = (ym_odds_evens) * 1
print(ym_01)</pre></code>

The resulting matrix is given below:

![image](https://user-images.githubusercontent.com/95583564/150122861-8b226eb8-dc97-43f5-b6ce-4d81c8b7979f.png)

## Q2.2

To visualise the values stored in ym_01 a heatmap was created with a colorbar. The image was saved as ym01_heatmap.png with an image quality of 600 dpi.

<pre><code>plt.imshow(ym_01, cmap='hot', interpolation='nearest')
plt.colorbar()
plt.savefig('ym01_heatmap.png', dpi=600)
plt.show()</pre></code>

The resulting heatmap:

![ym01_heatmap](https://user-images.githubusercontent.com/95583564/150123289-259a906d-0819-4b01-8b38-6bbe197ec133.png)
