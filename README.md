Graylog3 supported
------------------

Content Pack includes:
- Couple new GROK patern files
  * CISCO_MNEMONIC_FIRSTPART
  * CISCO_MNEMONIC_LASTPART
- Extractors for syslog messages
  * Supported new fields in search:
    CISCO_MESSAGE = Full syslog message
    CISCO_MNEMONIC_FIRSTPART = Mnemonic first part like SYS, LINK or PARSER
    CISCO_MNEMONIC_LASTPART = Mnemonic last part like MODEM_UP, CONFIG_I or UPDOWN
    CISCO_MNEMONIC = Full Mnemonic like SYS-5-CONFIG_I, LINEPROTO-5-UPDOWN or CISCO800-2-MODEM_UP
- Basic dashboard called Cisco "Switches And Routers"
  * 10 Most Used MNEMONICS 1 Day
  * 10 Least Used MNEMONICS 1 Day
  * Cisco Syslog Levels 1 Day
  * Top 10 Syslog Senders 1 Day
  * 10 Least Common MSG 1 Day
  * 10 Most Common MSG 1 Day
  * Number of Messages per hour
  **** NOTE START ****
  * Edit search query source if needed, default is "gl2_source_input:5cc199348a66df5bf971ef41"
  **** NOTE END ****
- Default input port is 1515


Cisco syslog config example:
#logging origin-id ip
#logging source-interface <interface>
#logging host <graylog-server> transport udp port 1515

Happy logging,

/Ville
