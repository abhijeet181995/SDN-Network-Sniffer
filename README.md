# To-Do
* check if `sniff.py` is working fine or not
* Remove the comments from `ryu_sniffer.py`

# SDN-Network-Sniffer
Environment requirements -
* Python 3.8+ on controller machine and machine where mininet will run.
* Ryu Framework on machine which is to act as controller, install by:`pip3 install ryu`.
* On mininet machine, install scapy using command:`pip3 install scapy`.

Run commands in the order as they appear.
* To run controller: `ryu-manager ryu-sniffer.py --observe-links`.
    * For topology.py, switch number is `4` and sniffer port number is `1`.
* To run mininet topology: `sudo python3 topology.py <controller-ip>`.
* To start sniffer in mininet: `sniffer python3 sniff.py &`. To see options to sniff.py run `sniffer python3 sniff.py -h`
* Now exchange packets between hosts in mininet, they will be recorded by the sniffer but will not be displayed on mininet as it currently does not support background processes for hosts. 