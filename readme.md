# Uso de Route 53 de AWS

# Manos a la obra
1) Chequear la disponibilidad de tu dominio a registrar (vía Freenom o dnschecher.org)
2) Registrar un dominio disponible en freenom (https://www.freenom.com/es/index.html?lang=es)
3) Desde su cuenta en AWS, desde el servicio Route 53
    a) crear una zona hospedada para el dominio registrado en el punto anterior
    b) crear dos registros de tipo A que apunten a un balanceador de cargas a través de un alías y de política de enrutamiento 'Simple routing'. Un record name puede ser en blanco (sin nada) y el otro con www.
4) Cargar en Freenom las direcciones de DNS de AWS en tu registro de dominio en la opción nameservers personalizados.
5) Chequear la propagación de tu dominio registrado en https://dnschecker.org/
6) Probar desde tu navegador el acceso a tu dominio (el cual esta relacionado con el balanceador de cargas seleccionado en el punto 3).
7) Crear un certificado en AWS vía el servicio Certificate Manager.
8) Desde Certificate Manager copiar los CNAMEs generados y guardarlos en S3
9) Desde Route 53, desde el dominio creado, importar dichos CNAMEs (en nueva versión de Route 53 este proceso puede ser automática)
10) Revear toda la infraestuctura para soporte el protocolo https!!!
11) A disfrutar de tus webs seguras!!


## Links de interes

- ### ¿Problemas con Freenom? Registrar un dominio gratis en Freenom?
    https://www.youtube.com/watch?v=uFY6rI_M7Q0
    https://www.youtube.com/watch?v=3Uopc4AFjOY

- ### Registrar dominio gratis en Freenom y vincularlo con AWS 
    https://www.youtube.com/watch?v=LpHFSE3IEVE

- ### Chequear propagación de DNS a nivel global
    https://dnschecker.org/

- ### Obtener un certificado SSL gratuito en AWS
    https://www.youtube.com/watch?v=0Mqj6BBcbjU    


