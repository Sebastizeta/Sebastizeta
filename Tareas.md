- {
 "cells": [
  {
   "cell_type": "markdown",
   "id": "69f9abf4",
   "metadata": {},
   "source": [
    "# Company Sales"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "2d8931e0",
   "metadata": {},
   "source": [
    "## Ejercicio 1 "
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "id": "3cd79494",
   "metadata": {},
   "outputs": [],
   "source": [
    "import pandas as pd #Importar paquetes de panda para trabajar con datasheets\n",
    "import matplotlib.pyplot as plt #Importar matplotlib para ejecutar en las líneas de código"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "id": "42960613",
   "metadata": {},
   "outputs": [],
   "source": [
    "df = pd.read_csv ('company_sales_data.csv') #aqui se lee el documento con los datos"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 6,
   "id": "007910b1",
   "metadata": {},
   "outputs": [],
   "source": [
    "profitList = df ['total_profit'].tolist() #definimos que profit list corresponde a la columna de total profit\\\n",
    "monthList  = df ['month_number'].tolist() #Se define la variable lista de mes"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 8,
   "id": "eb816a98",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": 
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "plt.plot(monthList, profitList, label = 'Month-wise Profit data of last year') #Se introduce que tipo de variable va a tener nuestra gráfica\n",
    "plt.xlabel('Month number') #etiquetamos eje x\n",
    "plt.ylabel('Profit in dollar') #etiquetamos eje y\n",
    "plt.xticks(monthList) #son las divisiones en x\n",
    "plt.title('Company profit per month') #Título de la grafica\n",
    "plt.yticks([100000, 200000, 300000, 400000, 500000]) #son las divisiones en y\n",
    "plt.show()"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "bda5aedf",
   "metadata": {},
   "source": [
    "## Ejercicio 2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 12,
   "id": "91915a6f",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": 
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "plt.plot(monthList, profitList, label = 'Profit data of last year', \n",
    "      color='r', marker='o', markerfacecolor='k', \n",
    "      linestyle='--', linewidth=3) \n",
    "plt.xlabel('Month Number')\n",
    "plt.ylabel('Profit in dollar')\n",
    "plt.legend(loc='lower right') #ubicamos la leyenda en la esquina abajo\n",
    "plt.title('Company Sales data of last year')\n",
    "plt.xticks(monthList)\n",
    "plt.yticks([100000, 200000, 300000, 400000, 500000])\n",
    "plt.show()#Definimos parametros para la siguiente grafica, no hace falta ejecutar los comandos iniciales porque ya son parte del codigo"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "e1771798",
   "metadata": {},
   "source": [
    "## Ejercicio 3"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 18,
   "id": "badc4747",
   "metadata": {},
   "outputs": [],
   "source": [
    "faceCremSalesData   = df ['facecream'].tolist()\n",
    "faceWashSalesData   = df ['facewash'].tolist()\n",
    "toothPasteSalesData = df ['toothpaste'].tolist()\n",
    "bathingsoapSalesData   = df ['bathingsoap'].tolist()\n",
    "shampooSalesData   = df ['shampoo'].tolist()\n",
    "moisturizerSalesData = df ['moisturizer'].tolist() #definimos todas la variables y a que dato de nuestra datasheet corresponden"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 19,
   "id": "be065be3",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": 
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "plt.plot(monthList, faceCremSalesData,   label = 'Face cream Sales Data', marker='o', linewidth=3)\n",
    "plt.plot(monthList, faceWashSalesData,   label = 'Face Wash Sales Data',  marker='o', linewidth=3)\n",
    "plt.plot(monthList, toothPasteSalesData, label = 'ToothPaste Sales Data', marker='o', linewidth=3)\n",
    "plt.plot(monthList, bathingsoapSalesData, label = 'ToothPaste Sales Data', marker='o', linewidth=3)\n",
    "plt.plot(monthList, shampooSalesData, label = 'ToothPaste Sales Data', marker='o', linewidth=3)\n",
    "plt.plot(monthList, moisturizerSalesData, label = 'ToothPaste Sales Data', marker='o', linewidth=3) #se le coloca el color y forma deseada a cada linea de la grafica, es decir a cada producto\n",
    "plt.xlabel('Month Number')\n",
    "plt.ylabel('Sales units in number')\n",
    "plt.legend(loc='upper left')\n",
    "plt.xticks(monthList)\n",
    "plt.yticks([1000, 2000, 4000, 6000, 8000, 10000, 12000, 15000, 18000])\n",
    "plt.title('Sales data') #se termina de definir el formato de la grafica similar a las de arriba\n",
    "plt.show()"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "f5b137f5",
   "metadata": {},
   "source": [
    "## Ejercicio 4"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 17,
   "id": "8ee4b6b4",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": 
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "plt.scatter(monthList, toothPasteSalesData, label = 'Tooth paste Sales data') #se escoje el nuevo grafico, no es necesario definir las variables usadas en otros graficos de nuevo\n",
    "plt.xlabel('Month Number')\n",
    "plt.ylabel('Number of units Sold')\n",
    "plt.legend(loc='upper left')\n",
    "plt.title(' Tooth paste Sales data')\n",
    "plt.xticks(monthList)\n",
    "plt.grid(True, linewidth= 1, linestyle=\"--\")\n",
    "plt.show()"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "5e23720b",
   "metadata": {},
   "source": [
    "## Ejercicio 5"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 20,
   "id": "fb97c929",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": 
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "plt.bar([a-0.25 for a in monthList], faceCremSalesData, width= 0.25, label = 'Face Cream sales data', align='edge') #escojemos grafico de barras\n",
    "plt.bar([a+0.25 for a in monthList], faceWashSalesData, width= -0.25, label = 'Face Wash sales data', align='edge') #las variables ya se definieron en ejercicios anteriores\n",
    "plt.xlabel('Month Number')\n",
    "plt.ylabel('Sales units in number')\n",
    "plt.legend(loc='upper left')\n",
    "plt.title(' Sales data')\n",
    "\n",
    "plt.xticks(monthList)\n",
    "plt.grid(True, linewidth= 1, linestyle=\"--\")\n",
    "plt.title('Facewash and facecream sales data')\n",
    "plt.show()\n"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "1f98f5b8",
   "metadata": {},
   "source": [
    "## Ejercicio 6"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 22,
   "id": "65a32d41",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": 
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "plt.bar(monthList, bathingsoapSalesData) #grafica de barras solo de un producto\n",
    "plt.xlabel('Month Number')\n",
    "plt.ylabel('Sales units in number')\n",
    "plt.title(' Sales data')\n",
    "plt.xticks(monthList)\n",
    "plt.grid(True, linewidth= 1, linestyle=\"--\")\n",
    "plt.title('bathingsoap sales data')\n",
    "plt.savefig('sales_data_of_bathingsoap.png', dpi=150) #guardar el grafico como imagen en la misma carpeta en que trabajamos\n",
    "plt.show()"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "375c6b52",
   "metadata": {},
   "source": [
    "## Ejercicio 7"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 23,
   "id": "abcb8ebe",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": 
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "labels = ['low', 'average', 'Good', 'Best']\n",
    "profit_range = [150000, 175000, 200000, 225000, 250000, 300000, 350000]\n",
    "plt.hist(profitList, profit_range, label = 'Profit data') #se selecciona el histograma\n",
    "plt.xlabel('profit range in dollar')\n",
    "plt.ylabel('Actual Profit in dollar')\n",
    "plt.legend(loc='upper left')\n",
    "plt.xticks(profit_range)\n",
    "plt.title('Profit data')\n",
    "plt.show()"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "c945a56b",
   "metadata": {},
   "source": [
    "## Ejercicio 8"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 24,
   "id": "1a30fd78",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": 
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "labels = ['FaceCream', 'FaseWash', 'ToothPaste', 'Bathing soap', 'Shampoo', 'Moisturizer']\n",
    "salesData   = [df ['facecream'].sum(), df ['facewash'].sum(), df ['toothpaste'].sum(), \n",
    "         df ['bathingsoap'].sum(), df ['shampoo'].sum(), df ['moisturizer'].sum()] #porcentajes de cada producto\n",
    "plt.axis(\"equal\")\n",
    "plt.pie(salesData, labels=labels, autopct='%1.1f%%') #grafico circular\n",
    "plt.legend(loc='lower right')\n",
    "plt.title('Sales data')\n",
    "plt.show()"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "ae8627c8",
   "metadata": {},
   "source": [
    "## Ejercicio 9"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 30,
   "id": "531f7533",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": 
      "text/plain": [
       "<Figure size 432x288 with 2 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "f, axarr = plt.subplots(2, sharex=True) #hacemos los dos graficos a la par\n",
    "axarr[0].plot(monthList, bathingsoapSalesData, label = 'Bathingsoap Sales Data', color='k', marker='o', linewidth=3) #se definen caracteristicas del primer grafico\n",
    "axarr[0].set_title('Sales data of  a Bathingsoap')\n",
    "axarr[1].plot(monthList, faceWashSalesData, label = 'Face Wash Sales Data', color='r', marker='o', linewidth=3) #se definen caracteristicas del segundo grafico\n",
    "axarr[1].set_title('Sales data of  a facewash') #titulo\n",
    "\n",
    "plt.xticks(monthList)\n",
    "plt.xlabel('Month Number')\n",
    "plt.ylabel('Sales units in number')\n",
    "plt.show()"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "3a276f6a",
   "metadata": {},
   "source": [
    "## Ejercicio 10"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 32,
   "id": "2995c204",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": 
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "plt.plot([],[],color='m', label='Face Cream', linewidth=5)\n",
    "plt.plot([],[],color='c', label='Face wash', linewidth=5)\n",
    "plt.plot([],[],color='r', label='Tooth paste', linewidth=5)\n",
    "plt.plot([],[],color='k', label='Bathing soap', linewidth=5)\n",
    "plt.plot([],[],color='g', label='Shampoo', linewidth=5)\n",
    "plt.plot([],[],color='y', label='Moisturizer', linewidth=5) #colores para cada dato\n",
    "\n",
    "plt.stackplot(monthList, faceCremSalesData, faceWashSalesData, toothPasteSalesData, \n",
    "              bathingsoapSalesData, shampooSalesData, moisturizerSalesData, \n",
    "              colors=['m','c','r','k','g','y']) #tipo de grafico\n",
    "\n",
    "plt.xlabel('Month Number')\n",
    "plt.ylabel('Sales unints in Number')\n",
    "plt.title('All product sales data using stack plot')\n",
    "plt.legend(loc='upper left')\n",
    "plt.show()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "8b854ea9",
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "69dc4b36",
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.8.8"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
