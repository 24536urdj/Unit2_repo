#.  
        from matplotlib import pyplot as plt
    import requests
    import numpy as np
    from numpy import polyfit
    import matplotlib.cm as cm

    req = requests.get("http://192.168.6.142/readings")
    data = req.json()
    print(data)
    for i in range(0, 1):
        readings = data["readings"][i]
    x = []
    T = []
    for r in readings:
        if r['sensor_id'] == 1:
            T.append(r["value"])
            x.append(r["datetime"])
    print(T)
    temp = T[610:800]
    x_noun = []
    for i in range(len(temp)):
        x_noun.append(i)
    m, b = np.polyfit(x_noun, temp, 1)
    y_linear = []
    for i in [0, x_noun[-1]]:
        y_linear.append(m * i + b)

    plt.plot([0, x_noun[-1]], y_linear, color="black")

    plt.scatter(x_noun, temp)
    plt.show()
