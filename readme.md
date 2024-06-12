currently  with these kind of setups, you can deploy each service seprately.
no need to studio, you can check and test your ws with realtime itself.
services should go up : db, kong, realtime

look at docker-compose as an example of how you should name your container and write your dockerfiles.

the name of realtime app should be realtime-dev, there is some thing in supabase that app names should be equal to name of those containers in docker-compose file

you can look at .env.example file to check for env you needs and get them if you don't have.
you can get a jwt signature token from supabase site itself, aware that I checked other kind of jwt ( such as from node.js) and they didn't worked out

for a better debug, make some app in supabase site itself and generate jwt, service key and anon key from there.

we need to clear dockerfiles and env and docker-compose from unused materials
also aware that because services are slightely coupled, you should update your env based on your services after deployment. (such as host name of db, kong, etc.)

service key and anon key are about 10-years long keys, no need to worry for updating them on a daily basis.

current jwt,service and anon key generated at 2024/7/12

#JWT_SECRET ="MxFP4SYNDw5LUE2ORvEOCd7lJtN3mxoHZMlg7DzrSUEzqUTzRjb8VoCF90aGx1TLK/J2x6zPuTaih/7tFuPhUA=="

#ANON_KEY ="eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6Im1jYmd0Z3ptZGdpdXN5bGx0aXh6Iiwicm9sZSI6ImFub24iLCJpYXQiOjE3MTgxOTUxMzEsImV4cCI6MjAzMzc3MTEzMX0.U2jZ6rXmXuaXwramicZWFNRHvIMitcoKuF8sdls5a-s"

#SERVICE_ROLE_KEY ="eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6Im1jYmd0Z3ptZGdpdXN5bGx0aXh6Iiwicm9sZSI6InNlcnZpY2Vfcm9sZSIsImlhdCI6MTcxODE5NTEzMSwiZXhwIjoyMDMzNzcxMTMxfQ.zuOrkNkDDmO0V15E3G71Y1AUN8Bs0dutP1r7E2RVkb0"

# **TODO**
this doc should be completed later as we clean and complete process of deploy and using supabase realtime

for chcking the complete version, beside files in here, look at created apps in `console.hamravesh.com/darkube` site -> `tank` org -> `tank` namespace

