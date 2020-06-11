# MT21104_17MT30001_30002
This Repository has been created for the submission of our Term Assignment for the course of Genetic Algorithms in Engineering Process Modelling.
*Hybrid Ant Colony Optimization, Genetic Algorithm, and Simulated Annealing for Image Contrast Enhancement*
The MATLAB code for enhancing the contrast of gray-scale images using nature-inspired methods can be found in this repo. The nature inspired methods are ant colony optimization, genetic algorithm, and simulated annealing, which generate a global transfer function to convert input images to higher contrast ones, while trying to keep the natural look of the images.

The method works by placing a few artificial agents (aka artificial ants) in a search space to generate a transfer function useful for converting any image to a higher contrast one.

After reaching the last point, a transfer function is created and its fitness is evaluated. Based on how good is a transfer function, pheromones are deposited on the path the ants have travelled. Pheromone on a point increases the chance of an ant in the next iteration to choose passing over it when nearby.

The Code
The MATLAB code in the file imenhance.m, under the im-enhance folder, contains the function to perform the image contrast enhancement. The function takes the input image and two optional arguments, one for the number of iterations and the other for disabling the simulated annealing if preferred to increase speed and probably at some performance cost.
