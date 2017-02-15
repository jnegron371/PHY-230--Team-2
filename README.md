# PHY-230--Team-2

    import numpy as np
    import matplotlib.pyplot as plt
    import math

    def pi(numDarts):
        plt.figure(1)
        area = 15
        N = 6545231
        x = np.random.rand(N)
        y = np.random.rand(N)
        circle = 0

        for i in range(numDarts):
            a = x[i]
            b = y[i]
        
            d = np.sqrt(a**2+b**2)

            if d <= 1:
                circle = circle + 1
                plt.plot(a, b, 'go')
            else:
                plt.plot(a, b, 'ro')
            
        pival = circle/numDarts * 4
        print(pival)
        plt.scatter(a, b, s=area, alpha=.5)
        #LaTeX markup can be used in your Python plots
        plt.title('$value of \pi$')
        #plt.text("$\pi= pi$")
        plt.show()
    
        pi(900)

