# PHY-230--Team-2

    import numpy as np
    import matplotlib.pyplot as plt
    import math

    def pi(numDarts):
        plt.figure(1) #creates a figure
        area = 15
        N = 6545231
        x = np.random.rand(N)
        y = np.random.rand(N)
        circle = 0

        for i in range(numDarts):
            a = x[i]
            b = y[i]
        
            d = np.sqrt(a**2+b**2) #coordinate of the dart

            if d <= 1:
                circle = circle + 1
                plt.plot(a, b, 'go') #the dart is in the circle
            else:
                plt.plot(a, b, 'ro') #the dart is outside of the circle
            
        pival = circle/numDarts * 4
        print(pival) #prints estimation of pi
        
        #Displays the graph
        plt.scatter(a, b, s=area, alpha=.5)
        
        #Graph title
        plt.title('$value of \pi$')
        plt.text("$\pi= pi$")
        plt.show()
    
        pi(900)

