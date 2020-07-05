# wiflex_00
token authentication (login, logout, register , reset password, change password) django , django-rest-framework

#endpoints 

 1. /rest-auth/login/ (POST)
 
  			1.username
			2.email
			3.password
			Returns Token Key
			
    
	
	
 2./rest-auth/logout/ (POST)
 	
	To logout the current user(send post request) (deletes the token in the database)
	to keep the user logged in after password change,just add following statement in project's  settings.py 
	LOGOUT_ON_PASSWORD_CHANGE = False
	
	
 3. /rest-auth/password/reset/ (POST)
 
  			1.email
			
 4. /rest-auth/password/rest/confirm (POST)
 
 			1.uid
			2.token
			3.new_password1
			4.new_password2
		(Uid and token are sent in email after calling /rest-auth/password/reset/
		
	(i am logging out the user after the password change)	
		
 5.   /rest-auth/password/change/ (POST)
 
 			1.new_password1
			2.new_password2
			
 6.   /rest-auth/user/(GET,PUT.PATCH)
 			
			1.username
			2.first_name
			3.last_name
			Return pk, username, email, first_name, last_name
			
 7. /rest-auth/registration/ (POST)
 
 		1.username
		2.password1
		3.password2
		4.email
		
		
8. /rest-auth/registration/verify-email  (POST)

	1.key
 
 
	
	
