# Install instructions

1) install npm

2) npm install --global yarn

3) npm install -g wrangler

npm install --save-dev ajv    ?

4) yarn wrangler dev --local




## Admin token

add local admin key to worker config in index.ts:

if (env.KARAOKEQ && (await env.KARAOKEQ.get('a_jiri')) == null) {
await env.KARAOKEQ.put('a_jiri', 'my-local-token');
}

where 'a_jiri' is the local domain and 'my-local-token' the password you want to use for admins.