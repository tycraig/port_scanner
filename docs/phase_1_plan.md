# Phase 1 - Implement a basic port scanner

### Research:
- Sockets in C++ (POSIX?)
- Error handling

### Plan:
1. Create outline/pseudocode
2. Identify test cases
3. Develop iteratively

### Outline
```
parse_user_input() {                    // use library for this?
    ip_address = arg[1];

    if(input contains -r) {
        range = arg[r];
    } else {
        range = scan_all_ip;
    }

    if(input contains -t) {
        timeout = arg[t]
    } else {
        timeout = default_timeout;
    }

    return ip, range, timeout;
}

main {
    ip, range, timeout = parse_user_input();

    for(each port in socket_range) {
        create_socket();
        attempt_connection();
        record_results;
    }

    out_results();
}
```

### Test cases
- Scan a single known port that is open
- Scan a single known port that is closed
- Scanning a range of ports on a service
- Handling invalid input for different flags