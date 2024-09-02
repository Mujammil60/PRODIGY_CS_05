# PRODIGY_CS_05
This is a simple GUI-based Network Sniffer application built using Python's tkinter and scapy libraries. The application allows users to select a network interface and start sniffing packets on that interface. The captured packets' details are displayed in the GUI, including IP addresses, protocols, and port numbers.

Features
Interface Selection: Choose from available network interfaces to monitor.
Packet Sniffing: Capture and display details of IP packets, including source and destination IPs, protocols, and TCP port information.
Real-time Display: Packets are displayed in real-time within the application's GUI.
Requirements
Python 3.x
tkinter (usually included with Python)
scapy library
You can install the required scapy library using pip:

bash
Copy code
pip install scapy
How to Run
Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/network-sniffer.git
cd network-sniffer
Run the application:

bash
Copy code
python network_sniffer.py
Use the Application:

The application will list all available network interfaces.
Select an interface from the dropdown menu.
Click "Start Sniffing" to begin capturing packets on the selected interface.
The captured packet details will be displayed in the text area below.
Code Overview
get_available_interfaces(): Retrieves a list of available network interfaces on the system.
start_sniffing(): Starts a separate thread to sniff packets on the selected interface.
sniff_packets(interface): Captures packets on the specified interface and processes each packet using process_packet().
process_packet(packet): Extracts information such as IP addresses, protocol, and ports from each packet and displays it in the GUI.
update_output(packet_info): Updates the text area in the GUI with the captured packet details.
