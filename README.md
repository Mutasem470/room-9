# room-9
Data Normalization - Prepare Sensor Data for Comparison 
You have sensor data from diff. machines. The readings are
on diff. scales, transform it to be consistent for comparison.

This function normalizes the sensor data using min-max scaling to bring all values into a 0 to 1 range for easy comparison.

 def transform(data):
    # Calculate the minimum and maximum values
    min_val = min(data)
    max_val = max(data)
    # Normalize data to a 0-1 scale
    normalized = [(x - min_val) / (max_val - min_val) for x in data]
    return normalized

# Sensor data with varying ranges
sensor_data = [500, 1200, 3000, 8000]

# Normalize the sensor data
normalized_data = transform(sensor_data)

print(f"Normalized data: {normalized_data}")
