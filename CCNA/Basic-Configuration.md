### Router Memory Types
    1.ROM
    2.NVRAM(Nonvolatile RAM)
    3.Flash RAM
    4.RAM

### Cisco Router mode

    1.User Execution mode(User EXEC--Router>enable)
    2.Privileged Execution mode(Privileged Execution mode--Router#config t)
    3.Global Configuration mode(Router(config)#)

Note: Transliting error promptly recover 

    ctrl+shift+6

    For permantly set
    ->(config)#no ip domain-lookup
    ->(config)#hostname(To set routername)

### To set welcome message(Banner)

    Router(config)#banner ?
    login  Set login banner
    motd   Set Message of the Day banner
    Router(config)#banner motd &
    Enter TEXT message.  End with the character '&'.
    &

    Router(config)#banner motd ?
    LINE  c banner-text c, where 'c' is a delimiting character
    Router(config)#banner motd c
    Enter TEXT message.  End with the character 'c'

### To set Password in console

    ->(config)#line console 0(which interface to login)
    ->(config-line)#password cisco(Set password)
    ->(config-line)#login

### To set password in telnet
 
    ->(config)#line vty 0 15(vty is telnet interface)
    ->(config-line)#password telnet(Set password)
    ->(config-line)#login

### To set password priviliged execution mode to global execution mode

    ->(config)#enable password ccna(Set password Execution mode to previleged mode)
    ->(config)#service password-encryption
    ->(config)#enable secret ccnp(Set Strong Password)


### To check status:
    
    ->#show running-config(sh run)
    ->show startup-config(sh start)


### Save ram to nvram

    ->#copy run start

