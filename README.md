# supabase-codespace-cors

```bash
# terminal 1
supabase start
supabase functions serve --no-verify-jwt --debug

# terminal 2
cd frontend
npm install
npm run dev # open developer tools and look at the network tab

echo $GITHUB_TOKEN # should start with ghu_

curl -i --location --request OPTIONS 'https://fluffy-waddle-r754gq645xcw79g-54321.app.github.dev//functions/v1/hello-world' \
    --header 'X-Github-Token: '$GITHUB_TOKEN
    
curl -i --location --request POST 'https://fluffy-waddle-r754gq645xcw79g-54321.app.github.dev//functions/v1/hello-world' \
    --header 'X-Github-Token: '$GITHUB_TOKEN
```
