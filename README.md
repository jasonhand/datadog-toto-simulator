# Datadog TOTO Simulator

A browser-based interactive simulator for understanding Datadog's **TOTO** (Time-Series-Optimized Transformer for Observability) foundational model. This simulator provides hands-on exploration of TOTO's capabilities in time series forecasting and observability metrics analysis.

## What is TOTO?

**TOTO** (Time-Series-Optimized Transformer for Observability) is Datadog's foundational model for time series forecasting and observability. It's a decoder-only transformer architecture specifically designed for monitoring infrastructure, networking, databases, and application metrics.

### Key Features of TOTO:

- **Foundation Model**: Pre-trained on 2+ trillion time series data points - the largest dataset for any open-weights time series model
- **Zero-Shot Forecasting**: Can forecast time series without fine-tuning on specific data
- **Multi-Variate Support**: Efficiently processes multiple variables using Proportional Factorized Space-Time Attention
- **Probabilistic Predictions**: Generates both point forecasts and uncertainty estimates using a Student-T mixture model
- **Observability Focus**: Specifically designed for monitoring metrics covering infrastructure, networking, databases, and applications
- **High Performance**: State-of-the-art results on GIFT-Eval benchmark and custom BOOM observability dataset

## How the Simulator Works

This interactive simulator demonstrates TOTO's capabilities through three main components:

### 1. Zero-Shot Forecasting Demo
- **Interactive Controls**: Adjust prediction length (24-336 hours), time series patterns, and confidence levels
- **Pattern Types**: 
  - Seasonal (CPU Usage patterns)
  - Trending (Memory Usage patterns)
  - Volatile (Network Traffic patterns)
  - Anomaly (with injected anomalies)
- **Uncertainty Bands**: Visualize probabilistic predictions with confidence intervals
- **Anomaly Injection**: Click on the chart or use the "Add Anomaly" button to simulate real-world anomalies
- **Performance Metrics**: Real-time MAE, MAPE, and coverage statistics

### 2. Multi-Variate Analysis
- **Variable Count**: Simulate 2-7 correlated observability metrics
- **Correlation Control**: Adjust the strength of relationships between variables
- **Time Windows**: Analyze different time periods (24 hours, 48 hours, 1 week)
- **Correlation Matrix**: Visual representation of variable relationships
- **Incident Simulation**: Simulate system incidents affecting multiple metrics simultaneously

### 3. Interactive Model Playground
- **Architecture Parameters**:
  - Context Length (512-4096 tokens)
  - Attention Heads (4-16 heads)
  - Model Size (Small: 70M, Base: 200M, Large: 500M parameters)
- **Performance Metrics**: Real-time inference speed, memory usage, and accuracy
- **Architecture Visualization**: Interactive visualization of the transformer layers
- **Dynamic Updates**: See how parameter changes affect model performance

## Technical Architecture

The simulator uses:
- **Chart.js**: For interactive time series visualizations
- **Vanilla JavaScript**: For model simulation and parameter handling
- **CSS Grid & Flexbox**: For responsive, modern UI design
- **Gradient Backgrounds**: For visually appealing interface

## Getting Started

1. **Open the Simulator**: Simply open `index.html` in any modern web browser
2. **Explore Zero-Shot Forecasting**: 
   - Select different time series patterns
   - Adjust prediction length and confidence levels
   - Click "Generate Forecast" to see TOTO's predictions
   - Add anomalies to see how the model responds
3. **Experiment with Multi-Variate Analysis**:
   - Change the number of variables
   - Adjust correlation strength
   - Simulate incidents to see cross-metric effects
4. **Tune Model Parameters**:
   - Modify context length, attention heads, and model size
   - Observe how changes affect performance metrics
   - Explore the architecture visualization

## Model Architecture

TOTO uses a decoder-only transformer architecture with:
- **Input Layer**: Processes time series data with positional encoding
- **Multi-Head Attention**: Uses Proportional Factorized Space-Time Attention for efficient multi-variate processing
- **Output Layer**: Generates probabilistic forecasts with uncertainty estimates

The model supports variable prediction horizons and context lengths, making it flexible for different observability use cases.

## Use Cases

This simulator helps understand TOTO's applications in:
- **Infrastructure Monitoring**: CPU, memory, disk, and network metrics
- **Application Performance**: Response times, error rates, throughput
- **Database Monitoring**: Query performance, connection pools, cache hit rates
- **Network Observability**: Traffic patterns, latency, packet loss
- **Anomaly Detection**: Identifying unusual patterns in time series data

## Production Availability

TOTO is available on Hugging Face with optimizations for:
- **xformers**: For efficient attention computation
- **flash-attention**: For memory-optimized attention
- **Custom inference**: For production deployment

## Contributing

This simulator is designed for educational purposes to help understand TOTO's capabilities. Feel free to:
- Experiment with different parameters
- Add new visualization features
- Improve the model simulation accuracy
- Extend the demo with additional TOTO features

## License

This project is licensed under the MIT License - see the LICENSE file for details.
