# eee-361-homework-4-denoising-random-sampling-and-admm-solved
**TO GET THIS SOLUTION VISIT:** [EEE-361 Homework 4-Denoising random sampling and ADMM Solved](https://www.ankitcodinghub.com/product/eee-361-homework-4-denoising-random-sampling-and-admm-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;94166&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;EEE-361 Homework 4-Denoising random sampling and ADMM Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
Sparse Signals and Denoising:

Here we will attempt to denoise a sparse signal that is corrupted by random noise. Generate a 1 × 128 vector, x, with 5 non-zero ([1:5]/5) coefficients and permute them randomly. Add random Gaussian noise with standard deviation σ = 0.05 to the signal to obtain y = x + n, where n ← σ ∗ randn(1,128). We will solve:

argmin21∥xˆ−y∥2 +λ∥xˆ∥1 xˆ

It turns out that this is very easy to solve. Because the variables xˆi, for 1 ≤ i ≤ 128 are independent, we can minimize each of them separately by solving

argmin12∥xˆi−yi∥2+λ∥xˆi∥1 , xˆi

for all 1 ≤ i ≤ 128. Find the closed form solution to each xˆi. Describe what happens when yi is small compared to λ, and when yi is large. Find solutions for λ = {0.01, 0.05, 0.1, 0.2}, and include the plot the error between actual sparse x and the obtained ones.

Random Frequency Domain Sampling and Aliasing

We’ll now explore the importance of incoherent sampling. First, compute the centered Fourier transform of the sparse signal, X = F x where F is a Fourier transform operator, i.e. X = fftc(x).

In compressed sensing, we undersample the measurements. We measure a subset of k-space, Xu = Fux where Fu is a Fourier transform evaluated only at a subset of frequency domain samples. This is an under- determined data set for which there is an infinite number of possible signals. However, we do know that the original signal is sparse, so there is hope we will be able to reconstruct it. The theory of compressed sensing suggests random undersampling. To see why, we will look at equispaced undersampling and compare it to random undersampling.

Undersample k-space by taking 32 equispaced samples. Compute the inverse Fourier transform, filling the missing data with zeroes, and multiply by 4 to correct for the fact that we have only 1/4 of the samples, i.e.

X u = zeros(1,128); X u(1:4:128) = X (1:4:128); xu = ifftc(X u)*4 .

Show that this is the Minimum Norm Least Squares solution. Plot the absolute value of the result and comment

on it.

Now, undersample k-space by taking 32 samples at random. Compute the zero-filled inverse Fourier trans-

form and multiply by 4 again:

Xr = zeros(1,128); prm = randperm(128); Xr(prm(1:32)) = X(prm(1:32)); xr = ifftc(Xr)*4 .

Plot the absolute value, and comment on it. How does this resemble the denoising problem? Note that the “noise” is not really noise, but incoherent aliasing that is contributed by the signal itself. Therefore, we might be able EXACTLY recover the sparse signal.

Reconstruction from Randomly Sampled Frequency Domain Data

Inspired by the denoising example, we will add an 1-norm penalty and solve argmin12∥Fuxˆ−y∥2 +λ∥xˆ∥1

xˆ

In this case, xˆ is the estimated signal, F uxˆ is the undersampled Fourier transform of the estimate, and y are the samples of the Fourier transform that we have acquired. Now the variables are coupled through the Fourier transform, and there is no closed-form solution. Solve this Lasso formulation by using ADMM. Make a plot of error between the true x and F uxˆ as a function of the iteration number, plotting the result for each of the λ = {0.01, 0.05, 0.1} . To plot the signal at each iteration use DRAWNOW after the plot command.

</div>
</div>
<div class="layoutArea">
<div class="column">
1

</div>
</div>
</div>
