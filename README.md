# github
Es un script en bash, que nos ayuda en la actualización de un repositorio,
esta pensado para añadirlo en .bashrc al final y lo grabas.

PASOS de la Instalación:

cd
gedit .bashrc
source .bashrc

# FIN instalado

PASOS ejecución
En tu terminal o consola escribe:
github

#- copia codigo y lo añades -#

function github(){
echo -e "\e[44m Actualiza Repositorio Github \e[49m"

cd 
mkdir app
cd ./app/
echo -e "\e[42mAñade la url ej:\e[49m Factoria-F5-AI-Bootcamp-1-Edicion/IATale.git"
read leeme
git clone https://github.com/$leeme
echo -e "\e[43mAñade carpeta: IATale\e[49m"
read carpeta
cd $carpeta
git add .
echo -e "\e[43mAñade comentario:\e[49m"
read comentario
git commit -m "Comentario"
echo -e "\e[42mActualizando...\e[49m"
git pull https://github.com/$leeme
git push
echo -e "\e[41mProceso terminado.\e[49m"
}



