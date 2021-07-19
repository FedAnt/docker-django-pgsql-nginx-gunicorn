# docker-django-pgsql-nginx-gunicorn
This is the template setup docker code for: 
- django with function upload and gunicorn
- postgresql
- nginx

# Start
docker-compose -f docker-compose.prod.yml up -d --build
docker-compose -f docker-compose.prod.yml exec web python manage.py migrate --noinput

# Stop
docker-compose -f docker-compose.prod.yml down -v