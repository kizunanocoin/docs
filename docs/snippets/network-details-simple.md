!!! info "Network Ports Overview"
	* **3975 TCP:** For [live network](/glossary#live-network) activity (since V19.0) and [bootstrap network](/glossary#bootstrap-network) activity
	* **3976 TCP:** For communication with RPC server. **Do not expose this outside of your production environment. Anyone with access to this port can control your node's RPC.**
	* **3978 TCP:** For communication with [websocket server](/integration-guides/websockets). Depending on configuration, data throughput can be very high.
	* **3975 UDP:** For [live network](/glossary#live-network) activity (fallback since V19.0, deprecated and disabled V21+)
	
--8<-- "udp-deprecated.md"
