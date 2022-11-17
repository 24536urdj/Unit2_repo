###
     def produce(n: object = 100,m=3,s=2) -> object:
        x_out = []
        y_out = []

        st = -10
        for i in range(100):
            x = st
            x_out.append(x)
            y = x**(-1/2*(m/s)**2)
            y_out.append(y)
            y_str = f"{y:.2f}"
            st += 0.2
            print(f"|{str(x).center(10)}|{y_str.center(10)}")

          return y_out, x_out


    sample = produce(n=5)

    from matplotlib import pyplot as plt

    data_y, data_x = produce(n=5)
    plt.plot(data_x, data_y, color="yellow", marker="*")
    plt.xlabel("Variable x")
    plt.ylabel("$x**(-1/2*(m/s)**2)}$")
    plt.show()
![](quiz11.jpg)
