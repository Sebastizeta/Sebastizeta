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


"Parte 2"
{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "90f81a72",
   "metadata": {},
   "source": [
    "# Automobile_Data"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "8b3c3335",
   "metadata": {},
   "source": [
    "## Ejercicio 1"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 1,
   "id": "21b74452",
   "metadata": {},
   "outputs": [],
   "source": [
    "import pandas as pd #importamos panda\n",
    "df = pd.read_csv(\"Automobile_data.csv\") #leemos el documento y lo definimos como df"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 2,
   "id": "52ca2c15",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>index</th>\n",
       "      <th>company</th>\n",
       "      <th>body-style</th>\n",
       "      <th>wheel-base</th>\n",
       "      <th>length</th>\n",
       "      <th>engine-type</th>\n",
       "      <th>num-of-cylinders</th>\n",
       "      <th>horsepower</th>\n",
       "      <th>average-mileage</th>\n",
       "      <th>price</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>0</td>\n",
       "      <td>alfa-romero</td>\n",
       "      <td>convertible</td>\n",
       "      <td>88.6</td>\n",
       "      <td>168.8</td>\n",
       "      <td>dohc</td>\n",
       "      <td>four</td>\n",
       "      <td>111</td>\n",
       "      <td>21</td>\n",
       "      <td>13495.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>1</td>\n",
       "      <td>alfa-romero</td>\n",
       "      <td>convertible</td>\n",
       "      <td>88.6</td>\n",
       "      <td>168.8</td>\n",
       "      <td>dohc</td>\n",
       "      <td>four</td>\n",
       "      <td>111</td>\n",
       "      <td>21</td>\n",
       "      <td>16500.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>2</td>\n",
       "      <td>alfa-romero</td>\n",
       "      <td>hatchback</td>\n",
       "      <td>94.5</td>\n",
       "      <td>171.2</td>\n",
       "      <td>ohcv</td>\n",
       "      <td>six</td>\n",
       "      <td>154</td>\n",
       "      <td>19</td>\n",
       "      <td>16500.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>3</td>\n",
       "      <td>audi</td>\n",
       "      <td>sedan</td>\n",
       "      <td>99.8</td>\n",
       "      <td>176.6</td>\n",
       "      <td>ohc</td>\n",
       "      <td>four</td>\n",
       "      <td>102</td>\n",
       "      <td>24</td>\n",
       "      <td>13950.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>4</td>\n",
       "      <td>audi</td>\n",
       "      <td>sedan</td>\n",
       "      <td>99.4</td>\n",
       "      <td>176.6</td>\n",
       "      <td>ohc</td>\n",
       "      <td>five</td>\n",
       "      <td>115</td>\n",
       "      <td>18</td>\n",
       "      <td>17450.0</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "   index      company   body-style  wheel-base  length engine-type  \\\n",
       "0      0  alfa-romero  convertible        88.6   168.8        dohc   \n",
       "1      1  alfa-romero  convertible        88.6   168.8        dohc   \n",
       "2      2  alfa-romero    hatchback        94.5   171.2        ohcv   \n",
       "3      3         audi        sedan        99.8   176.6         ohc   \n",
       "4      4         audi        sedan        99.4   176.6         ohc   \n",
       "\n",
       "  num-of-cylinders  horsepower  average-mileage    price  \n",
       "0             four         111               21  13495.0  \n",
       "1             four         111               21  16500.0  \n",
       "2              six         154               19  16500.0  \n",
       "3             four         102               24  13950.0  \n",
       "4             five         115               18  17450.0  "
      ]
     },
     "execution_count": 2,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.head() #vemos las primeras 5 lineas, no hace falta poner nada entre parentesis porque automatico muestra 5"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "id": "bb8e8bad",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>index</th>\n",
       "      <th>company</th>\n",
       "      <th>body-style</th>\n",
       "      <th>wheel-base</th>\n",
       "      <th>length</th>\n",
       "      <th>engine-type</th>\n",
       "      <th>num-of-cylinders</th>\n",
       "      <th>horsepower</th>\n",
       "      <th>average-mileage</th>\n",
       "      <th>price</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>56</th>\n",
       "      <td>81</td>\n",
       "      <td>volkswagen</td>\n",
       "      <td>sedan</td>\n",
       "      <td>97.3</td>\n",
       "      <td>171.7</td>\n",
       "      <td>ohc</td>\n",
       "      <td>four</td>\n",
       "      <td>85</td>\n",
       "      <td>27</td>\n",
       "      <td>7975.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>57</th>\n",
       "      <td>82</td>\n",
       "      <td>volkswagen</td>\n",
       "      <td>sedan</td>\n",
       "      <td>97.3</td>\n",
       "      <td>171.7</td>\n",
       "      <td>ohc</td>\n",
       "      <td>four</td>\n",
       "      <td>52</td>\n",
       "      <td>37</td>\n",
       "      <td>7995.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>58</th>\n",
       "      <td>86</td>\n",
       "      <td>volkswagen</td>\n",
       "      <td>sedan</td>\n",
       "      <td>97.3</td>\n",
       "      <td>171.7</td>\n",
       "      <td>ohc</td>\n",
       "      <td>four</td>\n",
       "      <td>100</td>\n",
       "      <td>26</td>\n",
       "      <td>9995.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>59</th>\n",
       "      <td>87</td>\n",
       "      <td>volvo</td>\n",
       "      <td>sedan</td>\n",
       "      <td>104.3</td>\n",
       "      <td>188.8</td>\n",
       "      <td>ohc</td>\n",
       "      <td>four</td>\n",
       "      <td>114</td>\n",
       "      <td>23</td>\n",
       "      <td>12940.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>60</th>\n",
       "      <td>88</td>\n",
       "      <td>volvo</td>\n",
       "      <td>wagon</td>\n",
       "      <td>104.3</td>\n",
       "      <td>188.8</td>\n",
       "      <td>ohc</td>\n",
       "      <td>four</td>\n",
       "      <td>114</td>\n",
       "      <td>23</td>\n",
       "      <td>13415.0</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "    index     company body-style  wheel-base  length engine-type  \\\n",
       "56     81  volkswagen      sedan        97.3   171.7         ohc   \n",
       "57     82  volkswagen      sedan        97.3   171.7         ohc   \n",
       "58     86  volkswagen      sedan        97.3   171.7         ohc   \n",
       "59     87       volvo      sedan       104.3   188.8         ohc   \n",
       "60     88       volvo      wagon       104.3   188.8         ohc   \n",
       "\n",
       "   num-of-cylinders  horsepower  average-mileage    price  \n",
       "56             four          85               27   7975.0  \n",
       "57             four          52               37   7995.0  \n",
       "58             four         100               26   9995.0  \n",
       "59             four         114               23  12940.0  \n",
       "60             four         114               23  13415.0  "
      ]
     },
     "execution_count": 3,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.tail() #vemos las ultimas 5 lineas, no hace falta poner nada entre parentesis porque automatico muestra 5"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "1dcf5f41",
   "metadata": {},
   "source": [
    "## Ejercicio 2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 5,
   "id": "5f373688",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "    index      company   body-style  wheel-base  length engine-type  \\\n",
      "0       0  alfa-romero  convertible        88.6   168.8        dohc   \n",
      "1       1  alfa-romero  convertible        88.6   168.8        dohc   \n",
      "2       2  alfa-romero    hatchback        94.5   171.2        ohcv   \n",
      "3       3         audi        sedan        99.8   176.6         ohc   \n",
      "4       4         audi        sedan        99.4   176.6         ohc   \n",
      "..    ...          ...          ...         ...     ...         ...   \n",
      "56     81   volkswagen        sedan        97.3   171.7         ohc   \n",
      "57     82   volkswagen        sedan        97.3   171.7         ohc   \n",
      "58     86   volkswagen        sedan        97.3   171.7         ohc   \n",
      "59     87        volvo        sedan       104.3   188.8         ohc   \n",
      "60     88        volvo        wagon       104.3   188.8         ohc   \n",
      "\n",
      "   num-of-cylinders  horsepower  average-mileage    price  \n",
      "0              four         111               21  13495.0  \n",
      "1              four         111               21  16500.0  \n",
      "2               six         154               19  16500.0  \n",
      "3              four         102               24  13950.0  \n",
      "4              five         115               18  17450.0  \n",
      "..              ...         ...              ...      ...  \n",
      "56             four          85               27   7975.0  \n",
      "57             four          52               37   7995.0  \n",
      "58             four         100               26   9995.0  \n",
      "59             four         114               23  12940.0  \n",
      "60             four         114               23  13415.0  \n",
      "\n",
      "[61 rows x 10 columns]\n"
     ]
    }
   ],
   "source": [
    "na_values={\n",
    "'price':[\"?\",\"n.a\"],\n",
    "'stroke':[\"?\",\"n.a\"],\n",
    "'horsepower':[\"?\",\"n.a\"],\n",
    "'peak-rpm':[\"?\",\"n.a\"],\n",
    "'average-mileage':[\"?\",\"n.a\"]} #buscamos todos los datos ? y n/a\n",
    "print (df) #imprimimos el dato\n",
    "\n",
    "df.to_csv(\"Automobile_data.csv\") #se modifica el documento"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "abb21cd9",
   "metadata": {},
   "source": [
    "## Ejercicio 3"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 6,
   "id": "b9bb6751",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>company</th>\n",
       "      <th>price</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>35</th>\n",
       "      <td>mercedes-benz</td>\n",
       "      <td>45400.0</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "          company    price\n",
       "35  mercedes-benz  45400.0"
      ]
     },
     "execution_count": 6,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df = df [['company','price']][df.price==df['price'].max()] #se busca el dato maximo en la columna de precio\n",
    "df #se imprime el dato"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "7404175c",
   "metadata": {},
   "source": [
    "## Ejercicio 4"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 8,
   "id": "b7cd36a1",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Unnamed: 0</th>\n",
       "      <th>index</th>\n",
       "      <th>company</th>\n",
       "      <th>body-style</th>\n",
       "      <th>wheel-base</th>\n",
       "      <th>length</th>\n",
       "      <th>engine-type</th>\n",
       "      <th>num-of-cylinders</th>\n",
       "      <th>horsepower</th>\n",
       "      <th>average-mileage</th>\n",
       "      <th>price</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>48</th>\n",
       "      <td>48</td>\n",
       "      <td>66</td>\n",
       "      <td>toyota</td>\n",
       "      <td>hatchback</td>\n",
       "      <td>95.7</td>\n",
       "      <td>158.7</td>\n",
       "      <td>ohc</td>\n",
       "      <td>four</td>\n",
       "      <td>62</td>\n",
       "      <td>35</td>\n",
       "      <td>5348.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>49</th>\n",
       "      <td>49</td>\n",
       "      <td>67</td>\n",
       "      <td>toyota</td>\n",
       "      <td>hatchback</td>\n",
       "      <td>95.7</td>\n",
       "      <td>158.7</td>\n",
       "      <td>ohc</td>\n",
       "      <td>four</td>\n",
       "      <td>62</td>\n",
       "      <td>31</td>\n",
       "      <td>6338.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>50</th>\n",
       "      <td>50</td>\n",
       "      <td>68</td>\n",
       "      <td>toyota</td>\n",
       "      <td>hatchback</td>\n",
       "      <td>95.7</td>\n",
       "      <td>158.7</td>\n",
       "      <td>ohc</td>\n",
       "      <td>four</td>\n",
       "      <td>62</td>\n",
       "      <td>31</td>\n",
       "      <td>6488.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>51</th>\n",
       "      <td>51</td>\n",
       "      <td>69</td>\n",
       "      <td>toyota</td>\n",
       "      <td>wagon</td>\n",
       "      <td>95.7</td>\n",
       "      <td>169.7</td>\n",
       "      <td>ohc</td>\n",
       "      <td>four</td>\n",
       "      <td>62</td>\n",
       "      <td>31</td>\n",
       "      <td>6918.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>52</th>\n",
       "      <td>52</td>\n",
       "      <td>70</td>\n",
       "      <td>toyota</td>\n",
       "      <td>wagon</td>\n",
       "      <td>95.7</td>\n",
       "      <td>169.7</td>\n",
       "      <td>ohc</td>\n",
       "      <td>four</td>\n",
       "      <td>62</td>\n",
       "      <td>27</td>\n",
       "      <td>7898.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>53</th>\n",
       "      <td>53</td>\n",
       "      <td>71</td>\n",
       "      <td>toyota</td>\n",
       "      <td>wagon</td>\n",
       "      <td>95.7</td>\n",
       "      <td>169.7</td>\n",
       "      <td>ohc</td>\n",
       "      <td>four</td>\n",
       "      <td>62</td>\n",
       "      <td>27</td>\n",
       "      <td>8778.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>54</th>\n",
       "      <td>54</td>\n",
       "      <td>79</td>\n",
       "      <td>toyota</td>\n",
       "      <td>wagon</td>\n",
       "      <td>104.5</td>\n",
       "      <td>187.8</td>\n",
       "      <td>dohc</td>\n",
       "      <td>six</td>\n",
       "      <td>156</td>\n",
       "      <td>19</td>\n",
       "      <td>15750.0</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "    Unnamed: 0  index company body-style  wheel-base  length engine-type  \\\n",
       "48          48     66  toyota  hatchback        95.7   158.7         ohc   \n",
       "49          49     67  toyota  hatchback        95.7   158.7         ohc   \n",
       "50          50     68  toyota  hatchback        95.7   158.7         ohc   \n",
       "51          51     69  toyota      wagon        95.7   169.7         ohc   \n",
       "52          52     70  toyota      wagon        95.7   169.7         ohc   \n",
       "53          53     71  toyota      wagon        95.7   169.7         ohc   \n",
       "54          54     79  toyota      wagon       104.5   187.8        dohc   \n",
       "\n",
       "   num-of-cylinders  horsepower  average-mileage    price  \n",
       "48             four          62               35   5348.0  \n",
       "49             four          62               31   6338.0  \n",
       "50             four          62               31   6488.0  \n",
       "51             four          62               31   6918.0  \n",
       "52             four          62               27   7898.0  \n",
       "53             four          62               27   8778.0  \n",
       "54              six         156               19  15750.0  "
      ]
     },
     "execution_count": 8,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df = pd.read_csv(\"Automobile_data.csv\")\n",
    "car_Manufacturers = df.groupby('company') #definimos a que linea corresponde car manufacturers\n",
    "toyotaDf = car_Manufacturers.get_group('toyota') #se busca en el grupo el dato toyota y se define como toyotaDf\n",
    "toyotaDf #se imprime el dato"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "2cb6d60b",
   "metadata": {},
   "source": [
    "## Ejercicio 5"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 9,
   "id": "64d1d2e7",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "toyota           7\n",
       "bmw              6\n",
       "mazda            5\n",
       "nissan           5\n",
       "mitsubishi       4\n",
       "mercedes-benz    4\n",
       "audi             4\n",
       "volkswagen       4\n",
       "honda            3\n",
       "isuzu            3\n",
       "jaguar           3\n",
       "alfa-romero      3\n",
       "chevrolet        3\n",
       "porsche          3\n",
       "dodge            2\n",
       "volvo            2\n",
       "Name: company, dtype: int64"
      ]
     },
     "execution_count": 9,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df = pd.read_csv(\"Automobile_data.csv\")\n",
    "df['company'].value_counts() #se cuenta por cuantas veces aparece el dato"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "313c8fbe",
   "metadata": {},
   "source": [
    "## Ejercicio 6"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 10,
   "id": "9ae01f42",
   "metadata": {},
   "outputs": [
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "<ipython-input-10-bfe5c082f322>:3: FutureWarning: Indexing with multiple keys (implicitly converted to a tuple of keys) will be deprecated, use a list instead.\n",
      "  priceDf = car_Manufacturers['company','price'].max() #se ubica el dato maximo por compañía y se define como price df\n"
     ]
    },
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>company</th>\n",
       "      <th>price</th>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>company</th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>alfa-romero</th>\n",
       "      <td>alfa-romero</td>\n",
       "      <td>16500.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>audi</th>\n",
       "      <td>audi</td>\n",
       "      <td>18920.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>bmw</th>\n",
       "      <td>bmw</td>\n",
       "      <td>41315.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>chevrolet</th>\n",
       "      <td>chevrolet</td>\n",
       "      <td>6575.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>dodge</th>\n",
       "      <td>dodge</td>\n",
       "      <td>6377.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>honda</th>\n",
       "      <td>honda</td>\n",
       "      <td>12945.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>isuzu</th>\n",
       "      <td>isuzu</td>\n",
       "      <td>6785.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>jaguar</th>\n",
       "      <td>jaguar</td>\n",
       "      <td>36000.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>mazda</th>\n",
       "      <td>mazda</td>\n",
       "      <td>18344.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>mercedes-benz</th>\n",
       "      <td>mercedes-benz</td>\n",
       "      <td>45400.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>mitsubishi</th>\n",
       "      <td>mitsubishi</td>\n",
       "      <td>8189.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>nissan</th>\n",
       "      <td>nissan</td>\n",
       "      <td>13499.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>porsche</th>\n",
       "      <td>porsche</td>\n",
       "      <td>37028.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>toyota</th>\n",
       "      <td>toyota</td>\n",
       "      <td>15750.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>volkswagen</th>\n",
       "      <td>volkswagen</td>\n",
       "      <td>9995.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>volvo</th>\n",
       "      <td>volvo</td>\n",
       "      <td>13415.0</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "                     company    price\n",
       "company                              \n",
       "alfa-romero      alfa-romero  16500.0\n",
       "audi                    audi  18920.0\n",
       "bmw                      bmw  41315.0\n",
       "chevrolet          chevrolet   6575.0\n",
       "dodge                  dodge   6377.0\n",
       "honda                  honda  12945.0\n",
       "isuzu                  isuzu   6785.0\n",
       "jaguar                jaguar  36000.0\n",
       "mazda                  mazda  18344.0\n",
       "mercedes-benz  mercedes-benz  45400.0\n",
       "mitsubishi        mitsubishi   8189.0\n",
       "nissan                nissan  13499.0\n",
       "porsche              porsche  37028.0\n",
       "toyota                toyota  15750.0\n",
       "volkswagen        volkswagen   9995.0\n",
       "volvo                  volvo  13415.0"
      ]
     },
     "execution_count": 10,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df = pd.read_csv(\"Automobile_data.csv\")\n",
    "car_Manufacturers = df.groupby('company') \n",
    "priceDf = car_Manufacturers['company','price'].max() #se ubica el dato maximo por compañía y se define como price df\n",
    "priceDf #se imprime el dato"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "1578a1b3",
   "metadata": {},
   "source": [
    "## Ejercicio 7"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 11,
   "id": "f4ca5662",
   "metadata": {},
   "outputs": [
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "<ipython-input-11-fb8d533957e3>:3: FutureWarning: Indexing with multiple keys (implicitly converted to a tuple of keys) will be deprecated, use a list instead.\n",
      "  mileageDf = car_Manufacturers['company','average-mileage'].mean() #se calcula el kilometraje promedio por compañia y se le define\n"
     ]
    },
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>average-mileage</th>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>company</th>\n",
       "      <th></th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>alfa-romero</th>\n",
       "      <td>20.333333</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>audi</th>\n",
       "      <td>20.000000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>bmw</th>\n",
       "      <td>19.000000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>chevrolet</th>\n",
       "      <td>41.000000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>dodge</th>\n",
       "      <td>31.000000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>honda</th>\n",
       "      <td>26.333333</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>isuzu</th>\n",
       "      <td>33.333333</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>jaguar</th>\n",
       "      <td>14.333333</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>mazda</th>\n",
       "      <td>28.000000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>mercedes-benz</th>\n",
       "      <td>18.000000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>mitsubishi</th>\n",
       "      <td>29.500000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>nissan</th>\n",
       "      <td>31.400000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>porsche</th>\n",
       "      <td>17.000000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>toyota</th>\n",
       "      <td>28.714286</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>volkswagen</th>\n",
       "      <td>31.750000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>volvo</th>\n",
       "      <td>23.000000</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "               average-mileage\n",
       "company                       \n",
       "alfa-romero          20.333333\n",
       "audi                 20.000000\n",
       "bmw                  19.000000\n",
       "chevrolet            41.000000\n",
       "dodge                31.000000\n",
       "honda                26.333333\n",
       "isuzu                33.333333\n",
       "jaguar               14.333333\n",
       "mazda                28.000000\n",
       "mercedes-benz        18.000000\n",
       "mitsubishi           29.500000\n",
       "nissan               31.400000\n",
       "porsche              17.000000\n",
       "toyota               28.714286\n",
       "volkswagen           31.750000\n",
       "volvo                23.000000"
      ]
     },
     "execution_count": 11,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df = pd.read_csv(\"Automobile_data.csv\")\n",
    "car_Manufacturers = df.groupby('company')\n",
    "mileageDf = car_Manufacturers['company','average-mileage'].mean() #se calcula el kilometraje promedio por compañia y se le define\n",
    "mileageDf #se imprime el dato"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "97b6986f",
   "metadata": {},
   "source": [
    "## Ejercicio 8"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 12,
   "id": "3c8d32a6",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Unnamed: 0</th>\n",
       "      <th>index</th>\n",
       "      <th>company</th>\n",
       "      <th>body-style</th>\n",
       "      <th>wheel-base</th>\n",
       "      <th>length</th>\n",
       "      <th>engine-type</th>\n",
       "      <th>num-of-cylinders</th>\n",
       "      <th>horsepower</th>\n",
       "      <th>average-mileage</th>\n",
       "      <th>price</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>35</th>\n",
       "      <td>35</td>\n",
       "      <td>47</td>\n",
       "      <td>mercedes-benz</td>\n",
       "      <td>hardtop</td>\n",
       "      <td>112.0</td>\n",
       "      <td>199.2</td>\n",
       "      <td>ohcv</td>\n",
       "      <td>eight</td>\n",
       "      <td>184</td>\n",
       "      <td>14</td>\n",
       "      <td>45400.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>11</th>\n",
       "      <td>11</td>\n",
       "      <td>14</td>\n",
       "      <td>bmw</td>\n",
       "      <td>sedan</td>\n",
       "      <td>103.5</td>\n",
       "      <td>193.8</td>\n",
       "      <td>ohc</td>\n",
       "      <td>six</td>\n",
       "      <td>182</td>\n",
       "      <td>16</td>\n",
       "      <td>41315.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>34</th>\n",
       "      <td>34</td>\n",
       "      <td>46</td>\n",
       "      <td>mercedes-benz</td>\n",
       "      <td>sedan</td>\n",
       "      <td>120.9</td>\n",
       "      <td>208.1</td>\n",
       "      <td>ohcv</td>\n",
       "      <td>eight</td>\n",
       "      <td>184</td>\n",
       "      <td>14</td>\n",
       "      <td>40960.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>46</th>\n",
       "      <td>46</td>\n",
       "      <td>62</td>\n",
       "      <td>porsche</td>\n",
       "      <td>convertible</td>\n",
       "      <td>89.5</td>\n",
       "      <td>168.9</td>\n",
       "      <td>ohcf</td>\n",
       "      <td>six</td>\n",
       "      <td>207</td>\n",
       "      <td>17</td>\n",
       "      <td>37028.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>12</th>\n",
       "      <td>12</td>\n",
       "      <td>15</td>\n",
       "      <td>bmw</td>\n",
       "      <td>sedan</td>\n",
       "      <td>110.0</td>\n",
       "      <td>197.0</td>\n",
       "      <td>ohc</td>\n",
       "      <td>six</td>\n",
       "      <td>182</td>\n",
       "      <td>15</td>\n",
       "      <td>36880.0</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "    Unnamed: 0  index        company   body-style  wheel-base  length  \\\n",
       "35          35     47  mercedes-benz      hardtop       112.0   199.2   \n",
       "11          11     14            bmw        sedan       103.5   193.8   \n",
       "34          34     46  mercedes-benz        sedan       120.9   208.1   \n",
       "46          46     62        porsche  convertible        89.5   168.9   \n",
       "12          12     15            bmw        sedan       110.0   197.0   \n",
       "\n",
       "   engine-type num-of-cylinders  horsepower  average-mileage    price  \n",
       "35        ohcv            eight         184               14  45400.0  \n",
       "11         ohc              six         182               16  41315.0  \n",
       "34        ohcv            eight         184               14  40960.0  \n",
       "46        ohcf              six         207               17  37028.0  \n",
       "12         ohc              six         182               15  36880.0  "
      ]
     },
     "execution_count": 12,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "carsDf = pd.read_csv(\"Automobile_data.csv\")\n",
    "carsDf = carsDf.sort_values(by=['price', 'horsepower'], ascending=False) #acomodamos los datos por precio\n",
    "carsDf.head() #imprimimos los primeros 5 datos"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "3b5be4f4",
   "metadata": {},
   "source": [
    "## Ejercicio 9"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 13,
   "id": "4a2b435a",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th>Company</th>\n",
       "      <th>Price</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th rowspan=\"4\" valign=\"top\">Germany</th>\n",
       "      <th>0</th>\n",
       "      <td>Ford</td>\n",
       "      <td>23845</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>Mercedes</td>\n",
       "      <td>171995</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>BMV</td>\n",
       "      <td>135925</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>Audi</td>\n",
       "      <td>71400</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th rowspan=\"4\" valign=\"top\">Japan</th>\n",
       "      <th>0</th>\n",
       "      <td>Toyota</td>\n",
       "      <td>29995</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>Honda</td>\n",
       "      <td>23600</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>Nissan</td>\n",
       "      <td>61500</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>Mitsubishi</td>\n",
       "      <td>58900</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "               Company   Price\n",
       "Germany 0         Ford   23845\n",
       "        1     Mercedes  171995\n",
       "        2          BMV  135925\n",
       "        3         Audi   71400\n",
       "Japan   0       Toyota   29995\n",
       "        1        Honda   23600\n",
       "        2       Nissan   61500\n",
       "        3  Mitsubishi    58900"
      ]
     },
     "execution_count": 13,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "GermanCars = {'Company': ['Ford', 'Mercedes', 'BMV', 'Audi'], 'Price': [23845, 171995, 135925 , 71400]} #definimos cuales carros son germancars\n",
    "carsDf1 = pd.DataFrame.from_dict(GermanCars) \n",
    "\n",
    "japaneseCars = {'Company': ['Toyota', 'Honda', 'Nissan', 'Mitsubishi '], 'Price': [29995, 23600, 61500 , 58900]} #definimos cuales carros son japanesecars\n",
    "carsDf2 = pd.DataFrame.from_dict(japaneseCars)\n",
    "\n",
    "carsDf = pd.concat([carsDf1, carsDf2], keys=[\"Germany\", \"Japan\"]) #se pone el nombre que debe aparecer o titulo por variable\n",
    "carsDf #se imprime"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "54f9a164",
   "metadata": {},
   "source": [
    "## Ejercicio 10"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 14,
   "id": "2914fca6",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Company</th>\n",
       "      <th>Price</th>\n",
       "      <th>horsepower</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>Toyota</td>\n",
       "      <td>23845</td>\n",
       "      <td>141</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>Honda</td>\n",
       "      <td>17995</td>\n",
       "      <td>80</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>BMV</td>\n",
       "      <td>135925</td>\n",
       "      <td>182</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>Audi</td>\n",
       "      <td>71400</td>\n",
       "      <td>160</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "  Company   Price  horsepower\n",
       "0  Toyota   23845         141\n",
       "1   Honda   17995          80\n",
       "2     BMV  135925         182\n",
       "3    Audi   71400         160"
      ]
     },
     "execution_count": 14,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "Car_Price = {'Company': ['Toyota', 'Honda', 'BMV', 'Audi'], 'Price': [23845, 17995, 135925 , 71400]}\n",
    "carPriceDf = pd.DataFrame.from_dict(Car_Price) #escojemos los carros por precio\n",
    "\n",
    "car_Horsepower = {'Company': ['Toyota', 'Honda', 'BMV', 'Audi'], 'horsepower': [141, 80, 182 , 160]} \n",
    "carsHorsepowerDf = pd.DataFrame.from_dict(car_Horsepower) #escojemos los carros por horsepower\n",
    "\n",
    "carsDf = pd.merge(carPriceDf, carsHorsepowerDf, on=\"Company\") #ubicamos las columnas y se unen para que solo se muestren estas\n",
    "carsDf #se imprime"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "2db0a914",
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
