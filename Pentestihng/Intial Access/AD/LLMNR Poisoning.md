link local multicast name resolution
What is the protocol?
	used to identify hosts when DNS fails to do so 
	previously NBT-NS
	key flaw is that the services utilize a user's username and NTLMv2 hash when appropriately responding to
using responder
	sudo responder -I (interface) -dwp
	-d DHCP
	-w wpad proxy server
	-P ProxyAuth
	-v verbose
