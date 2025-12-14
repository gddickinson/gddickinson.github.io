# GPS Tracker

Python script for handling GPS data and basic mapping functionality.

**GitHub:** [gddickinson/gps-tracker](https://github.com/gddickinson/gps-tracker)

---

## Overview

A comprehensive Python toolkit for GPS data processing, track analysis, and interactive mapping. Designed for outdoor enthusiasts, researchers, and developers working with GPS/GNSS data.

---

## Features

### GPS Data Processing
- **Multiple Format Support**: GPX, KML, CSV, NMEA
- **Data Parsing**: Extract waypoints, tracks, and routes
- **Coordinate Conversion**: WGS84, UTM, and other systems
- **Track Simplification**: Reduce point density while preserving shape
- **Quality Filtering**: Remove GPS errors and outliers

### Analysis Tools
- **Distance Calculation**: Total distance and segment distances
- **Elevation Analysis**: Gain/loss, grade, profiles
- **Speed Metrics**: Average, maximum, moving speed
- **Time Analysis**: Duration, moving time, stopped time
- **Statistical Summary**: Comprehensive track statistics

### Mapping & Visualization
- **Interactive Maps**: Web-based map viewers
- **Track Overlay**: Display routes on base maps
- **Elevation Profiles**: Height vs distance plots
- **Speed Graphs**: Velocity over time/distance
- **Waypoint Markers**: Points of interest display
- **Multiple Base Maps**: OpenStreetMap, satellite, terrain

### Offline Functionality
- **Tile Caching**: Download map tiles for offline use
- **Offline Routing**: Navigation without internet
- **Local Storage**: Self-contained track databases
- **Export Options**: Share data in multiple formats

---

## Installation

```bash
# Clone repository
git clone https://github.com/gddickinson/gps-tracker.git
cd gps-tracker

# Install dependencies
pip install gpxpy folium geopy numpy pandas matplotlib

# Run the tracker
python gps_tracker.py
```

---

## Usage

### Loading GPS Data

```python
from gps_tracker import GPSTracker

# Initialize tracker
tracker = GPSTracker()

# Load GPX file
track = tracker.load_gpx("my_hike.gpx")

# Load from CSV
track = tracker.load_csv("gps_data.csv")

# Load NMEA data
track = tracker.load_nmea("nmea_log.txt")
```

### Basic Analysis

```python
# Get track statistics
stats = tracker.analyze(track)

print(f"Distance: {stats['distance_km']:.2f} km")
print(f"Elevation gain: {stats['elevation_gain_m']:.0f} m")
print(f"Average speed: {stats['avg_speed_kmh']:.1f} km/h")
print(f"Duration: {stats['duration']}")
```

### Interactive Mapping

```python
# Create interactive map
map_obj = tracker.create_map(
    track,
    map_type='OpenStreetMap',
    show_waypoints=True,
    show_elevation_profile=True
)

# Save map
map_obj.save("my_track_map.html")
```

### Advanced Filtering

```python
# Remove GPS errors
clean_track = tracker.filter_outliers(
    track,
    max_speed_kmh=150,  # Remove unrealistic speeds
    max_gap_seconds=300  # Remove large time gaps
)

# Simplify track (reduce points)
simplified = tracker.simplify_track(
    track,
    tolerance=0.0001  # Douglas-Peucker algorithm
)
```

---

## Analysis Features

### Distance Metrics
```python
metrics = tracker.calculate_metrics(track)

# Available metrics
- total_distance: Overall track length
- segment_distances: Distance between each point
- cumulative_distance: Running total at each point
- straight_line_distance: Start to end distance
```

### Elevation Analysis
```python
elevation = tracker.analyze_elevation(track)

# Elevation data
- total_gain: Cumulative elevation gain
- total_loss: Cumulative elevation loss
- max_elevation: Highest point
- min_elevation: Lowest point
- avg_grade: Average slope percentage
- elevation_profile: Height vs distance array
```

### Speed Analysis
```python
speed_data = tracker.analyze_speed(track)

# Speed metrics
- avg_speed: Mean speed
- max_speed: Maximum recorded speed
- moving_avg_speed: Speed while moving
- speed_distribution: Histogram data
- speed_over_time: Time series
```

### Time Analysis
```python
time_stats = tracker.analyze_time(track)

# Time metrics
- total_duration: Total elapsed time
- moving_time: Time spent moving
- stopped_time: Time spent stopped
- pace_per_km: Minutes per kilometer
```

---

## Visualization Options

### Elevation Profile
```python
# Create elevation profile
fig = tracker.plot_elevation_profile(
    track,
    show_grade=True,
    highlight_climbs=True
)
fig.savefig("elevation_profile.png")
```

### Speed Graph
```python
# Plot speed over time
fig = tracker.plot_speed(
    track,
    smooth=True,
    show_moving_avg=True
)
```

### Interactive Map Types
- **OpenStreetMap**: Standard street map
- **Satellite**: Aerial imagery
- **Terrain**: Topographic features
- **Hybrid**: Satellite with labels

---

## Coordinate Systems

### Supported Formats
```python
# WGS84 (latitude/longitude)
lat, lon = 40.7128, -74.0060

# UTM (Universal Transverse Mercator)
zone, easting, northing = tracker.latlon_to_utm(lat, lon)

# Convert back
lat2, lon2 = tracker.utm_to_latlon(zone, easting, northing)
```

---

## Data Export

```python
# Export to different formats
tracker.export_gpx(track, "output.gpx")
tracker.export_kml(track, "output.kml")
tracker.export_csv(track, "output.csv")
tracker.export_geojson(track, "output.geojson")
```

---

## Offline Maps

### Downloading Tiles
```python
# Download map tiles for offline use
tracker.download_map_tiles(
    bounds=(lat_min, lon_min, lat_max, lon_max),
    zoom_levels=range(10, 16),
    map_source='OpenStreetMap'
)
```

### Using Offline Maps
```python
# Create map with offline tiles
map_obj = tracker.create_map(
    track,
    use_offline_tiles=True,
    tile_directory="./map_cache"
)
```

---

## API Reference

### Main Classes

```python
class GPSTracker:
    def load_gpx(filepath) -> Track
    def load_csv(filepath) -> Track
    def analyze(track) -> Dict
    def create_map(track, **kwargs) -> folium.Map
    def export_gpx(track, filepath) -> None
    
class Track:
    points: List[TrackPoint]
    name: str
    distance_km: float
    duration: timedelta
    
class TrackPoint:
    lat: float
    lon: float
    elevation: float
    time: datetime
    speed: float (optional)
```

---

## Configuration

### Default Settings
```python
config = {
    'default_map': 'OpenStreetMap',
    'distance_units': 'metric',  # or 'imperial'
    'elevation_units': 'meters',  # or 'feet'
    'speed_units': 'kmh',  # or 'mph'
    'timezone': 'UTC'
}
```

---

## Technical Stack

- **gpxpy**: GPX file parsing
- **folium**: Interactive mapping
- **geopy**: Coordinate operations
- **NumPy**: Numerical calculations
- **Pandas**: Data management
- **Matplotlib**: Plotting
- **Shapely**: Geometric operations

---

## Use Cases

- **Hiking/Running**: Track outdoor activities
- **Cycling**: Route analysis and planning
- **Research**: GPS data analysis
- **Fleet Management**: Vehicle tracking
- **Wildlife Tracking**: Animal movement studies
- **Field Work**: Scientific data collection

---

## Example Workflows

### Analyze a Hike
```python
# Load track
track = tracker.load_gpx("hike.gpx")

# Get statistics
stats = tracker.analyze(track)

# Create elevation profile
tracker.plot_elevation_profile(track)

# Create interactive map
map_obj = tracker.create_map(track)
map_obj.save("hike_map.html")
```

### Compare Multiple Routes
```python
# Load multiple tracks
tracks = [
    tracker.load_gpx("route1.gpx"),
    tracker.load_gpx("route2.gpx"),
    tracker.load_gpx("route3.gpx")
]

# Compare statistics
comparison = tracker.compare_tracks(tracks)

# Plot on same map
map_obj = tracker.create_comparison_map(tracks)
```

---

## Future Development

- Real-time GPS tracking
- Route planning and optimization
- Social features (share tracks)
- Mobile app integration
- Machine learning for activity recognition
- Integration with fitness APIs
- Advanced route analysis

---

*Comprehensive GPS data processing and mapping toolkit*
