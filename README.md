# how-to-learn-python

#1、画布配置

plt.figure(figsize=(5,3), dpi=300, facecolor='g')

#一个画布上画多个图

plt.plot(x, np.sin(x))

plt.plot(x, np.cos(x))

#使用subplot画多个图

x= np.linspace(0, np.pi)

y= np.sin(x)

ax1= plt.subplot(2,2,1)

ax1.plot(x,y)

ax1.set_title('子图1')

#双轴显示，并且标记不同的颜色

x= np.linspace(0, np.pi)

axes1=plt.gca()

axes1.plot(x, np.sin(x), color='r')

axes1.set_xlabel('time')

axes1.set_ylabel('sinx', c='r')

axes1.tick_params(axis='y', labelcolor='r')

axes2= axes1.twinx()

axes2.plot(x, np.cos(x), color='b')

axes2.set_ylabel('cosx', c='b')

axes2.tick_params(axis='y', labelcolor='b')

plt.tight_layout()

plt.show()


