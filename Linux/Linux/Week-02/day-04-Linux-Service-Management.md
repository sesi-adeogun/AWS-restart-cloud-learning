# AWS re/Start – Week 2, Day 4
## Linux Service Management and System Monitoring

**Date:** November 12, 2026  
**Learning Area:** Linux Administration  
**Environment:** AWS EC2 – Linux

---

## 1. Learning Objectives

Today's practical session focused on understanding Linux service management and monitoring system performance.

The objectives were to:

- Understand how Linux services are managed using `systemctl`.
- Check the operational status of the Apache HTTP Server.
- Start and manage Linux services.
- Monitor running processes and system resource utilisation.
- Understand system load averages and process activity.

## 2. Practical Exercise 1: Managing Apache HTTP Server

### Checking the Apache service status

I started by checking the status of the Apache HTTP Server using:

```bash
sudo systemctl status httpd.service
```

**Initial observation:**

The Apache HTTP Server was installed but its status showed:

```text
Active: inactive (dead)
```

This indicated that the service was not currently running.

### Starting the Apache service

I started the service using:

```bash
sudo systemctl start httpd.service
```

I then checked its status again:

```bash
sudo systemctl status httpd.service
```

**Result:**

The service successfully transitioned to:

```text
Active: active (running)
```

The output also showed that the Apache process was running.

### Commands learned

| Command | Purpose |
|---|---|
| `systemctl status httpd` | Check service status |
| `systemctl start httpd` | Start a service |
| `systemctl stop httpd` | Stop a service |
| `systemctl restart httpd` | Restart a service |
| `systemctl enable httpd` | Enable automatic startup at boot |
| `systemctl disable httpd` | Disable automatic startup at boot |

## 3. Practical Exercise 2: Linux System Monitoring

I used the Linux `top` command to monitor system performance and observe running processes.

```bash
top
```

### Initial system observations

During the initial monitoring session, I observed:

- 88 total tasks.
- CPU idle utilisation of approximately 99.8%.
- Low system activity.

### Observing system activity

During the subsequent practical exercise, a stress-test script was executed in the lab environment while monitoring system activity with `top`.

The observed system metrics included:

- 106 total tasks.
- 15 running tasks.
- A visible `stress` process.
- Load averages of approximately 13.97, 9.75 and 4.46.

The exercise demonstrated how system workload and process activity can change under increased resource demand.

The stress-test exercise subsequently completed.

## 4. Important Linux Commands

```bash
# Check Apache service status
sudo systemctl status httpd.service

# Start Apache
sudo systemctl start httpd.service

# Monitor system processes
top
```

## 5. Key Lessons Learned

Today's practical session strengthened my understanding of:

1. Linux service management and the role of systemd.
2. The difference between an inactive service and an active service.
3. Starting and monitoring Apache HTTP Server.
4. Using `top` to observe running processes and system performance.
5. Understanding system load averages and task counts.
6. The importance of monitoring system resources during increased workloads.

## 6. Practical Relevance to Cloud and DevOps Engineering

Linux service management and system monitoring are important skills in cloud infrastructure administration.

As a future Cloud and DevOps Engineer, these skills are useful for:

- Managing web servers hosted on AWS EC2.
- Troubleshooting services that fail to start.
- Monitoring server performance.
- Identifying resource-intensive processes.
- Supporting infrastructure reliability and availability.

## 7. Conclusion

Today's AWS re/Start practical session provided hands-on experience with Linux service management and system monitoring.

I successfully started the Apache HTTP Server, verified its running status, and explored Linux process monitoring using `top`.

These exercises reinforced the importance of Linux administration in managing cloud-based infrastructure.

---

**Tags:** #AWS #AWSRestart #LinuxAdministration #EC2 #Apache #SystemMonitoring #CloudComputing #DevOps #TechnicalLearning