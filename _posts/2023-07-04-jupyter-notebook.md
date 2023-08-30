---
layout: post
title: Numerical integration using Symbolic Python
date: 2023-08-29 03:45:00-0400
description: a blog post with jupyter notebook
tags: trapz riemann 
categories: sample-posts
giscus_comments: true
related_posts: false
---

<!--- To include a jupyter notebook in a post, you can use the following code:

{% raw %}

```html
{::nomarkdown}
{% assign jupyter_path = "assets/jupyter/blog.ipynb" | relative_url %}
{% capture notebook_exists %}{% file_exists assets/jupyter/blog.ipynb %}{% endcapture %}
{% if notebook_exists == "true" %}
    {% jupyter_notebook jupyter_path %}
{% else %}
    <p>Sorry, the notebook you are looking for does not exist.</p>
{% endif %}
{:/nomarkdown}
```

{% endraw %}
-->


<!--- Let's break it down: this is possible thanks to [Jekyll Jupyter Notebook plugin](https://github.com/red-data-tools/jekyll-jupyter-notebook) that allows you to embed jupyter notebooks in your posts. It basically calls [`jupyter nbconvert --to html`](https://nbconvert.readthedocs.io/en/latest/usage.html#convert-html) to convert the notebook to an html page and then includes it in the post. Since [Kramdown](https://jekyllrb.com/docs/configuration/markdown/) is the default Markdown renderer for Jekyll, we need to surround the call to the plugin with the [::nomarkdown](https://kramdown.gettalong.org/syntax.html#extensions) tag so that it stops processing this part with Kramdown and outputs the content as-is.

The plugin takes as input the path to the notebook, but it assumes the file exists. If you want to check if the file exists before calling the plugin, you can use the `file_exists` filter. This avoids getting a 404 error from the plugin and ending up displaying the main page inside of it instead. If the file does not exist, you can output a message to the user. The code displayed above outputs the following:

-->

When diving into the world of calculus, one of the fundamental concepts you'll encounter is the concept of approximating the area under a curve using sums. Two common types of approximations are left endpoint sums and right endpoint sums. These techniques play a crucial role in understanding integration and the behavior of functions.

## The Basics of Sums and Approximations

Imagine you have a curve on a graph, representing a function. The area under this curve between two points on the x-axis holds valuable information about the behavior of the function. But **how do we calculate this area when the curve isn't easily described by a simple mathematical formula?**

That's where approximations come in. By dividing the interval between two x-values into smaller subintervals, we can treat each subinterval as a rectangle and calculate the combined area of these rectangles to approximate the total area under the curve.

## Left Endpoint Sums

A left endpoint sum, also known as a left Riemann sum, approximates the area under the curve using the left endpoint of each subinterval. Here's how it works:

1. Divide the interval [a, b] into smaller subintervals of equal width.
2. For each subinterval, find the height of the rectangle by evaluating the function at the left endpoint of the subinterval.
3. Calculate the area of each rectangle by multiplying its height by the width of the subinterval.
4. Add up the areas of all the rectangles to approximate the total area under the curve.

Mathematically, the left endpoint sum for a function f(x) over the interval [a, b] with n subintervals is given by:


<!---
![alt text for screen readers](/assets/jupyter/L_n.png "In the left-endpoint approximation of area under a curve, the height of each rectangle is determined by the function value at the left of each subinterval")
-->
<p align="center">
<img src="/assets/jupyter/L_n.png" alt="In the left-endpoint approximation of area under a curve, the height of each rectangle is determined by the function value at the left of each subinterval." />
</p>

$$ A \approx L_n = f(x_0)\Delta x + f(x_1)\Delta x + \cdots f(x_{n-1})\Delta x = \sum_{i=1}^{n} f(x_{i-1}) \cdot \Delta x $$
 
where $$ \Delta x $$ is the width of each subinterval.

## Right Endpoint Sums

On the other hand, a right endpoint sum, or a right Riemann sum, approximates the area under the curve using the right endpoint of each subinterval. The process is similar to the left endpoint sum, but the heights of the rectangles are determined by evaluating the function at the right endpoints of the subintervals.

Mathematically, the right endpoint sum for a function f(x) over the interval [a, b] with n subintervals is given by:

<p align="center">
<img src="/assets/jupyter/R_n.png" alt="In the right-endpoint approximation of area under a curve, the height of each rectangle is determined by the function value at the right of each subinterval." />
</p>

$$ R_n = \sum_{i=1}^{n} f(x_i) \cdot \Delta x $$

## Comparing Left and Right Endpoint Sums

Left and right endpoint sums provide two different ways to approximate the area under a curve. Depending on the behavior of the function, the two approximations might yield slightly different results. In some cases, they might even converge to the actual area as the number of subintervals increases.

It's important to note that both left and right endpoint sums are types of Riemann sums, which are foundational to understanding the concept of integration. As you delve deeper into calculus, you'll discover that the definite integral of a function is the limit of these Riemann sums as the width of the subintervals approaches zero.



{::nomarkdown}
{% assign jupyter_path = "assets/jupyter/Post1_Integ.ipynb" | relative_url %}
{% capture notebook_exists %}{% file_exists assets/jupyter/Post1_Integ.ipynb %}{% endcapture %}
{% if notebook_exists == "true" %}
    {% jupyter_notebook jupyter_path %}
{% else %}
    <p>Sorry, the notebook you are looking for does not exist.</p>
{% endif %}
{:/nomarkdown}

## Conclusion

Left endpoint and right endpoint sums are valuable tools in the calculus toolkit. They provide a way to approximate the area under a curve when the function isn't easily integrated. These concepts pave the way for understanding integration, the fundamental theorem of calculus, and more advanced topics in calculus.

By grasping the fundamentals of left and right endpoint sums, you're taking the first steps toward a deeper comprehension of the intricate relationships between functions, their derivatives, and the areas they enclose.

So the next time you encounter a curve that seems elusive to integrate directly, remember that left and right endpoint sums are there to help you approximate and gain insights into its behavior.

