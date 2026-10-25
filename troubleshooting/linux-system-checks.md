# Linux System Troubleshooting Checks

## 1. Overview

This guide documents basic Linux commands used to inspect system resources, network connectivity, running processes, and disk space.

## 2. Check System Information

```bash
hostname
uptime
uname -r
```

- `hostname`: Displays the system hostname.
- `uptime`: Shows how long the system has been running and system load averages.
- `uname -r`: Displays the kernel release.

## 3. Check CPU and Memory

```bash
top
free -h
```

- `top`: Displays running processes and resource usage.
- `free -h`: Shows memory and swap usage.

## 4. Check Disk Space

```bash
df -h
du -sh /var/log
```

- `df -h`: Displays filesystem space usage.
- `du -sh /var/log`: Shows the total size of `/var/log`.

## 5. Check Network Connectivity

```bash
ip addr
ip route
ping -c 4 8.8.8.8
```

- `ip addr`: Displays network interfaces and IP addresses.
- `ip route`: Displays the routing table.
- `ping`: Tests basic IP connectivity to a destination.

A failed ping does not always mean the destination is down; ICMP traffic may be blocked.

## 6. Check DNS Resolution

```bash
getent hosts example.com
```

This checks whether the system can resolve a hostname using its configured name-resolution mechanisms.

## 7. Check Services and Logs

```bash
systemctl --failed
journalctl -p err -b
```

- `systemctl --failed`: Lists failed system services.
- `journalctl -p err -b`: Displays error-priority journal entries from the current boot.

Some systems may use different logging tools or service managers.

## 8. Troubleshooting Workflow

1. Identify the reported symptom.
2. Check system health and resource usage.
3. Verify the IP address and routing table.
4. Test connectivity to the relevant destination.
5. Check DNS if hostname resolution is failing.
6. Review relevant service status and logs.
7. Document findings and verify the result after any fix.

## 9. Practice Tasks

- Record your system's hostname and uptime.
- Check available memory and disk space.
- Identify your network interface and default route.
- Test connectivity to a permitted destination.
- Check for failed services and review relevant logs.

## Learning Notes

Add your own command output, observations, and troubleshooting examples after testing them in your Linux lab. Do not publish private IP details, credentials, or confidential system logs.
