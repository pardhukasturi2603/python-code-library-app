Clone the repo 

docker build -t dbimage database/ <br />
docker build -t authimage auth/ <br />
docker build -t bookimage book/ <br />
docker build -t borrowimage borrow/ <br />
docker build -t appimage . <br /> <br /> <br /> <br />


docker network create mynet <br /> <br /> <br /> <br />


docker run -d --name db -p 3306:3306 --network pardhu dbimage <br />
docker run -d --name auth_service --network pardhu  -p 5001:5001 authimage <br />
docker run -d --name book_service -p 5002:5002 --network pardhu bookimage <br />
docker run -d --name borrow_service  -p 5003:5003 --network pardhu borrowimage <br />
docker run -d --name frontend  -p 5000:5000 --network pardhu  appimage <br /> 

 
