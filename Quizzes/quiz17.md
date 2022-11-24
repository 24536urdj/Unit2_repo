# 
       def f(x=[]):
      if len(x) == 2:
          for i in range(2):
              out = x[0]
              out_1 = x[1]
              out_3 = (len(out_1) + len(out)) / 2
              print(out_3)
      else :
          for i in range(3) :
              out = x[0]
              out_1 = x[1]
              out_2 = x[2]
              out_3 = (len(out_1) + len(out)+len(out_2)) / 3
              print(out_3)



    f(["hello", "main","pilot"])
