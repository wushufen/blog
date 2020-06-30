
	location /weChatDistributionApi/ {
		proxy_pass http://weChatDistributionApiServer/;
		if ($request_method = 'OPTIONS') {
			add_header 'Access-Control-Allow-Origin' '*';
			add_header 'Access-Control-Allow-Headers' '*';
			add_header Access-Control-Allow-Methods GET,POST,OPTIONS,PATCH;
			return 204;
		}
	}
