# Call Cognitive - IBM 📞

Con Voice Agent de IBM es posible crear un call cognitive que nos permite tener interacciones de voz directas y automatizadas por teléfono entre sus clientes y un agente cognitivo. Con la inteligencia artificial de Watson como eje central, el agente puede comunicarse de forma más conversacional y manejar interacciones complejas difíciles para los sistemas tradicionales de respuesta de voz interactiva.

## 1. Pre Requisitos ⚠

- Tener una cuenta de IBM Cloud, sino la tiene puede crearla de forma gratuita. [IBM CLOUD](https://cloud.ibm.com/registration)

- Tener una cuenta de Twilio, sino la tiene por favor cree una. [TWILIO](https://www.twilio.com/try-twilio)

## 2. Componentes 📋 

- [Voice Agent](https://cloud.ibm.com/catalog/services/voice-agent-with-watson) : permite interacciones de voz directas y automatizadas por teléfono.

- [Speech to Text](https://cloud.ibm.com/catalog/services/speech-to-text) : Convierte el audio del interlocutor en texto.

- [Watson Assistant](https://cloud.ibm.com/catalog/services/watson-assistant) : Analiza el texto, lo correlaciona con intenciones y ofrece una respuesta en función de un diálogo que crea el usuario.

- [Text to Speech](https://cloud.ibm.com/catalog/services/text-to-speech)  : Convierte la respuesta en audio de voz.

## 3. Paso a Paso 👣

Para iniciar ingrese a IBM Cloud y adquiera los servicios que se encuentran en los componentes. 

En Twilio cree un Trunks:

![Captura de Pantalla 2020-10-14 a la(s) 8 33 58 a  m](https://user-images.githubusercontent.com/44415995/95998604-a4a20a00-0dfa-11eb-9980-14859a10e0ce.png)


Una vez creado el Trunk vamos a origination y agregamos la siguiente ORIGINATION URI ***sip:us-south.voiceagent.cloud.ibm.com***, guarde los cambios.

![Captura de Pantalla 2020-10-14 a la(s) 8 34 51 a  m](https://user-images.githubusercontent.com/44415995/95998599-a4097380-0dfa-11eb-961d-ed56846ccfec.png)

Adquiera un número en Twilio y cuando lo este creando es necesario que el Voice lo configure con SIP Trunk y elija el nombre del Trunk que acaba de crear.

![Captura de Pantalla 2020-10-14 a la(s) 8 48 45 a  m](https://user-images.githubusercontent.com/44415995/95998595-a2d84680-0dfa-11eb-8e67-35af308700f6.png)





1. Ingresamos a Watson Assistant donde creamos las intenciones necesarias para entrenar nuestras conversaciones. Una vez realizado el diálogo nos posicionamos en el nodo donde queremos que nuestro call cognitive inicie y colocamos la varible conversation_start. 

![Captura de Pantalla 2020-10-14 a la(s) 12 16 50 a  m](https://user-images.githubusercontent.com/44415995/95947004-54ec2000-0db3-11eb-9289-85ce44fd57f3.png)


2. Ingresamos al servicio de Voice Agent: Oprimimos el botón create an agent o crear agente en caso de que este en español:

![Captura de Pantalla 2020-10-13 a la(s) 11 02 03 p  m](https://user-images.githubusercontent.com/44415995/95942277-63810a00-0da8-11eb-8e6d-ec1915b01829.png)



3. Vamos a crear un nuevo agente así que escogemos  el tipo en este caso Voice (Voz) y llenamos los campos obligatorios como lo son el nombre y el nùmero celular, recuerde que este número previamente fue comprado por medio de Twilio.

![Captura de Pantalla 2020-10-13 a la(s) 11 10 06 p  m](https://user-images.githubusercontent.com/44415995/95942712-8364fd80-0da9-11eb-9b00-e910de504d3b.png)


4. En la sección de conversation, escogemos el tipo para este caso Watson Assistant y recuerde que la locación debe ser la misma donde creo el servicio de watson assistant. Adicionalmente escoga la instancia del servicio y el skill con que se trabajará. 
Nota --> Seleccione la opción de auto generar credenciales para que sea un proceso automatico.

![Captura de Pantalla 2020-10-13 a la(s) 11 24 56 p  m](https://user-images.githubusercontent.com/44415995/95943561-ccb64c80-0dab-11eb-9462-1c8844e3b6ea.png)

5. En la parte de Spech to text también escogemos el tipo, la locación acorde al servicio. El nombre que usted le quiera dar y el modelo y tipo de modelo que se usarán.

![Captura de Pantalla 2020-10-13 a la(s) 11 38 36 p  m](https://user-images.githubusercontent.com/44415995/95944558-0e47f700-0dae-11eb-9a0e-9621ebe7b264.png)

6. Llegamos a la sección de Text to spech donde debemos escoger el tipo de sercicio, el nombre la instancia del servicio y el tipo de voz que queramos que tenga nuestro call cognitivo.

![Captura de Pantalla 2020-10-13 a la(s) 11 53 28 p  m](https://user-images.githubusercontent.com/44415995/95945160-78ad6700-0daf-11eb-8563-74424ca2041d.png)

7. Finalmente oprimos el boton create a agent que se ecuentra en la parte superior y listo.
Es hora de llamar a probar nuestro call cognitive.

![Captura de Pantalla 2020-10-13 a la(s) 11 59 12 p  m](https://user-images.githubusercontent.com/44415995/95945487-2fa9e280-0db0-11eb-9aa4-19c3d8a33cec.png)





## Construido con 🛠️
- [IBM CLOUD](https://developer.ibm.com/technologies/artificial-intelligence/)

## Mas información 📖
- [Inteligencia artificial](https://www.ibm.com/cloud/)



## Autores ✒️
* **IBM** - *Equipo IBM Cloud*
