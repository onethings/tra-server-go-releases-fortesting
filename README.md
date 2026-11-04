sudo apt update && sudo apt install -y unzip

BASE=https://raw.githubusercontent.com/onethings/tra-server-go-releases-fortesting/main
curl -L -O "$BASE/traccar-server-go_0.1.0.zip"
curl -L -O "$BASE/traccar-server-go_0.1.0.zip.sha256"
sha256sum -c traccar-server-go_0.1.0.zip.sha256 # macOS: shasum -a 256 -c
unzip traccar-server-go_0.1.0.zip && cd traccar-server-go_0.1.0
sudo ./install.sh
