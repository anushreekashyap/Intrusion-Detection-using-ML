import random

print("=" * 40)
print("      INTRUSION DETECTION SYSTEM")
print("=" * 40)

# Store generated network traffic
network_data = []

# Generate 20 random network records
for i in range(20):
    duration = random.randint(1, 1000)
    src_bytes = random.randint(100, 10000)
    dst_bytes = random.randint(100, 10000)

    # Simple attack detection rule
    if duration > 900 or src_bytes > 8000:
        label = "Attack"
    else:
        label = "Normal"

    network_data.append([duration, src_bytes, dst_bytes, label])

# Display generated data
print("\nGenerated Network Traffic:\n")

for i, data in enumerate(network_data, start=1):
    print(f"{i}. Duration: {data[0]:4} | "
          f"Src Bytes: {data[1]:5} | "
          f"Dst Bytes: {data[2]:5} | "
          f"Status: {data[3]}")

print("\n" + "=" * 40)
print("      TEST CUSTOM NETWORK TRAFFIC")
print("=" * 40)

# User input
try:
    duration = int(input("Enter Duration: "))
    src_bytes = int(input("Enter Source Bytes: "))
    dst_bytes = int(input("Enter Destination Bytes: "))

    # Detection
    if duration > 900 or src_bytes > 8000:
        print("\nResult: ATTACK DETECTED")
    else:
        print("\nResult: NORMAL TRAFFIC")

except ValueError:
    print("\nPlease enter valid numeric values.")

print("\nSystem Finished Successfully")
