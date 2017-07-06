sudo apt-get update
sudo apt-get upgrade
sudo apt-get install asterisk git
cd
git clone  https://github.com/rgrokett/RaspiAsteriskGoogle.git
cd /home/pi/RaspiAsteriskGoogle
bash ./install.sh
// Intaller le Soft-Phone
cd /home/pi
nano /home/pi/client_secret.json
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install portaudio19-dev libffi-dev libssl-dev
sudo apt-get install python-pip
sudo easy_install pip

sudo python -m pip install --upgrade PySocks
sudo python -m pip install --upgrade google-assistant-grpc
sudo python -m pip install --upgrade google-auth-oauthlib 
sudo python -m pip install --upgrade urllib3[secure]
sudo python -m pip install --upgrade sounddevice
sudo python -m pip install --upgrade click
sudo python -m pip install --upgrade tenacity
sudo python -m pip install --upgrade google-auth-oauthlib[tool]
sudo python -m pip install --upgrade protobuf
sudo python -m pip install --upgrade googlesamples-assistant-pushtotalk

sudo reboot



google-oauthlib-tool --client-secrets /home/pi/client_secret.json --scope https://www.googleapis.com/auth/assistant-sdk-prototype --save --headless 



cd /home/pi/RaspiAsteriskGoogle
bash ./install.sh
bash ./test.sh
