# python-ping
a 2.7 and 3.4+ pure python ICMP ping implementation using raw sockets. from shell or from your code as a per node class. modded from https://pypi.python.org/pypi/python-ping/2011.10.17.376a019

## examples :
### from shell :

    c:\Python27\python.exe ping.py 192.168.0.254
    c:\Python34\python.exe ping.py 192.168.0.254

this should run on linux I didn't check yet, thanks for any feedback.

### from python console :

    # 3 verbose pings
    from ping import Ping
    h = Ping('www.google.com')
    h.run(3)

### from your module :

    # a simple 'is alive ?' one icmp request check
    from ping import IsUp
    box = IsUp('192.168.0.254') # returns a response time or False if something is wrong 
                                # unknown named host, no host, no socket, no network .. anything
    if box.isup() : thisIsCool()
    else : thisIsFrustrating()

IsUp is a subclass of Ping
