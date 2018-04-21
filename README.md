get    'auth/verify'   headers : {
  Authorization: 'bearer token_recieved_after_login'
}

# Get login token

post   'auth/login'   {
	"auth": {
		"email": "elhenimokhles@gmail.com",
		"password": "password"
	}
}

# User actions
get    '/users'  
get    '/users/current'   headers : {
  Authorization: 'bearer token_recieved_after_login'
}

post   '/users/create'  {
	"user": {
		"email": "elhenimokhles@gmail.com",
		"username": "mokhles elheni",
		"password": "password"
	}
}
patch  '/users/:id'       => 'users#update'
delete '/users/:id'       => 'users#destroy'
