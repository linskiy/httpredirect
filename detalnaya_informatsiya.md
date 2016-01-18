# Детальная информация
Вам нужно создать форму, которая использует POST URL  
```<form method="post" action="https://priceplan.pro/api/signup">  
  <!-- Secure parameters would go here here -->
  <!-- For brevity, this form contains no labels, only inputs :) -->
  <input type="hidden" name="signup[product][handle]" value="basic" />  
  <input type="text" name="signup[customer][first_name]" />  
  <input type="text" name="signup[customer][last_name]" />
  <input type="text" name="signup[customer][email]" />
  <input type="text" name="signup[payment_profile][first_name]" />
  <input type="text" name="signup[payment_profile][last_name]" />
  <input type="text" name="signup[payment_profile][card_number]" />
  <input type="text" name="signup[payment_profile][expiration_month]" />  
  <input type="text" name="signup[payment_profile][expiration_year]" />  
  <input type="submit" value="Sign Up" />
</form>```  
Код формы должен содержать параметры безопасности и параметры клиента и подписки, которую необходимо создать . Вы также можете добавить данные, которые API вернет обратно для того, чтобы их можно было показать клиенту на странице подтверждения.  


### После того как PricePlan получит POST  формы  


  * происходит подтверждение ключа подписи
  * PricePlan пытается создать слиента и подписку с параметрами формы
  * факт вызова API и его результат записывается в логах PricePlan
  


### После того как PricePlan создаст клиента и подписку.

РricePlan перебрасывает на ваш URL, который вы задали, добавляя параметры, указанные в POST. Поле этого ваш скрипт 
  * проверить ключ подписи
  * сгенерировать страницу успешной регистрации или ошибки, в зависимости от переданных параметров
  * факт вызова API и его результат записывается в логах PricePlan.
  






