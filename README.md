# Image Contrast Enhancement
The MATLAB code for enhancing the contrast of gray-scale images using nature-inspired methods can be found in this repo. The nature inspired methods are ant colony optimization, genetic algorithm, and simulated annealing, which generate a global transfer function to convert input images to higher contrast ones, while trying to keep the natural look of the images.

The method works by placing a few artificial agents (aka artificial ants) in a search space to generate a transfer function useful for converting any image to a higher contrast one. The ants start from the origin of the transfer function (bottom left) and move to the top right point of that.  Any ant probabilistically chooses among its available movement options, which are shown below:
<p align="center">
  <img src="./docs/ant.jpg" alt="Movement of ants on the transfer function pane" height=200/>
</p>

After reaching the last point, a transfer function is created and its fitness is evaluated. Based on how good is a transfer function, pheromones are deposited on the path the ants have travelled. Pheromone on a point increases the chance of an ant in the next iteration to choose passing over it when nearby. Here is an example of pheromone traces of ants after moving on a transfer function pane for a while.
<p align="center">
  <img src="./docs/pheromone.jpg" alt="Pheromone deposits of artificial ants" height=200/>
</p>

Each artificial ant has a genetic code during the process. The population of ants evolves via genetic algorithm. This changes the characteristics of the ants and their preferences in traversing their path in the search space. After selecting the best transfer functions, the simulated annealing tries to fine-tune them in an artificial annealing process. This is the flowchart of the general steps in the method:
<p align="center">
  <img src="./docs/flowchart.jpg" alt="Flowchart" height=350/>
</p>

After this process is finished, the best transfer function is selected and is used to convert the input image. Check these samples out:
<p align="center">
  <img src="./docs/example1.jpg" alt="Example 1" height=200/>
</p>
<p align="center">
  <img src="./docs/example2.jpg" alt="Example 2" height=200/>
    <br>
  <em>Left: original images, Right: after enhancement</em>
</p>

## The Code
The MATLAB code in the file *imenhance.m*, under the *im-enhance* folder, contains the function to perform the image contrast enhancement. The function takes the input image and two optional arguments, one for the number of iterations and the other for disabling the simulated annealing if preferred to increase speed and probably at some performance cost.

