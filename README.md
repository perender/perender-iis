# Integrating PERENDER with IIS (Internet Information Services)
![image](https://github.com/perender/perender-iis/assets/155614699/4e7ab024-5427-48ce-9dd2-33cb585f6af8)

IIS (Internet Information Services) es un servidor web desarrollado por Microsoft para sistemas operativos Windows. Su función principal es alojar y gestionar aplicaciones web, así como facilitar la comunicación entre los clientes web y los recursos del servidor.

# Step 1
<b>Prerequisites:</b>

<b>1.</b> Install and enable the URL Rewrite Module for IIS (https://www.iis.net/downloads/microsoft/url-rewrite)

<b>2.</b> Install and enable the Application Request Routing module for IIS (https://www.iis.net/downloads/microsoft/application-request-routing)

# Step 2.
<b>1.</b> Open the Internet Information Services (IIS) Manager.

<b>2.</b> Select your server (A).

<b>3.</b> Double-click on the URL Rewrite module (B).

![image](https://github.com/perender/perender-iis/assets/155614699/e2869b3d-36c5-4046-9ed4-d2e3f4bfee38)

# Step 3.
<b>1.</b> Select the View Server Variables... option (A).

![image](https://github.com/perender/perender-iis/assets/155614699/4ffd5c5b-a996-45ef-90f7-c0eac7ed113f)

# Step 4.
<b>1.</b> Select the Add... option (A).

![image](https://github.com/perender/perender-iis/assets/155614699/aca01322-5b35-4c7c-8c95-5066b2fd8cb6)

# Step 5.
<b>Add two variables:</b>

<b>1.</b> BOT_AGENT

<b>2.</b> HTTP_Authorization

![image](https://github.com/perender/perender-iis/assets/155614699/62142af6-e2d4-4fc9-87dd-c9180f24e5ec)

# Step 6.
<b>Now we will configure the Application Request Routing module installed in Step 1.</b>

<b>1.</b> Select your server (A).

<b>3.</b> Double-click on the Application Request Routing module (B).

![image](https://github.com/perender/perender-iis/assets/155614699/6fd699bf-63bd-41b7-91f7-00dad587aae2)

# Step 7.
<b>1.</b> Select the Server Proxy Settings... option (A).

![image](https://github.com/perender/perender-iis/assets/155614699/11b6e717-42f7-492c-b50c-2d99af23c874)

# Step 8.
<b>1.</b> Select the Enable proxy option (A).

<b>2.</b> Select the Apply option (B).

![image](https://github.com/perender/perender-iis/assets/155614699/7c62c4ca-33cd-46ee-90b4-271458aa0e3a)

# Step 9.
<b>1.</b> Navigate to the path where your website is hosted.

<b>2.</b> If your website does not have a web.config file, create one and paste the provided code below.

<b>3.</b> If your website already has a web.config file, simply add the PERENDER rule. <b>If your web.config has other rules, the PERENDER rule should be included at the top.</b>

<b>4.</b> Within the provided code, replace [PERENDER_TOKEN] with your token from the PERENDER dashboard.

Repository on GitHub at the following address https://github.com/perender/perender-iis/blob/main/web.config

