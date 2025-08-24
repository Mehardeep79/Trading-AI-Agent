# AI Trading Agent using Agentic AI

An autonomous AI trading agent built with Deep Q-Learning (DQN) that learns to make profitable trading decisions in the stock market. This project implements reinforcement learning techniques to create an intelligent agent capable of buying, selling, and holding stocks based on market conditions.

## 🚀 Features

- **Autonomous Decision Making**: AI agent makes independent trading decisions without human intervention
- **Deep Q-Learning**: Uses neural networks to approximate Q-values for optimal action selection
- **Technical Indicators**: Incorporates moving averages and returns for enhanced decision-making
- **Experience Replay**: Learns from past experiences to improve future performance
- **Exploration vs Exploitation**: Balances random exploration with learned strategies
- **Real Market Data**: Trained and tested on actual stock market data from Yahoo Finance

## 🏗️ Architecture

### Core Components

1. **Agent**: DQN-based decision-making entity
2. **Environment**: Stock market simulation with price movements
3. **State**: Market information (closing price, moving averages, returns)
4. **Action Space**: Three actions - BUY, SELL, HOLD
5. **Reward Function**: Maximizes total profit over trading sessions

### Neural Network Architecture

```
Input Layer (4 features) → Hidden Layer (64 neurons) → Hidden Layer (64 neurons) → Output Layer (3 actions)
```

## 📋 Requirements

```txt
yfinance>=0.2.18
pandas>=1.5.0
numpy>=1.24.0
torch>=2.0.0
```

## 🛠️ Installation

1. Clone the repository:
```bash
git clone https://github.com/Mehardeep79/Trading-AI-Agent.git
cd trading-ai-agent
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

## 📊 Performance

The AI agent demonstrates successful learning capabilities:

- **Initial Balance**: $10,000
- **Final Balance**: $32,908.82
- **Total Profit**: $22,908.82 
- **Training Episodes**: 500

## 🧠 How It Works

### 1. Data Collection
- Fetches historical stock data from Yahoo Finance
- Calculates technical indicators (SMA_5, SMA_20, Returns)
- Preprocesses data for neural network input

### 2. Environment Setup
- Simulates trading environment with balance and holdings tracking
- Provides rewards based on trading performance
- Manages state transitions and episode termination

### 3. Agent Training
- Uses epsilon-greedy strategy for exploration
- Stores experiences in replay buffer
- Updates neural network through backpropagation
- Gradually reduces exploration rate over time

### 4. Decision Making
- Analyzes current market state
- Predicts Q-values for each possible action
- Selects action with highest expected reward

## 📈 Technical Indicators

The agent uses the following features for decision-making:

- **Closing Price**: Current stock price
- **5-Day SMA**: Short-term moving average
- **20-Day SMA**: Long-term moving average  
- **Daily Returns**: Percentage change in price

## 🔧 Configuration

Key hyperparameters that can be tuned:

```python
gamma = 0.95           # Discount factor
epsilon = 1.0          # Initial exploration rate
epsilon_decay = 0.995  # Exploration decay rate
learning_rate = 0.001  # Neural network learning rate
batch_size = 32        # Training batch size
memory_size = 2000     # Experience replay buffer size
```

## 🚀 Future Enhancements

- [ ] Add more technical indicators (RSI, MACD, Bollinger Bands)
- [ ] Implement multiple stock trading
- [ ] Add portfolio management features
- [ ] Integrate real-time data streaming
- [ ] Implement risk management strategies
- [ ] Add visualization dashboard
- [ ] Support for cryptocurrency trading
- [ ] Implement other RL algorithms (A3C, PPO)


## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## 👨‍💻 Author

**Mehardeep Singh Sandhu**
- GitHub: [@Mehardeep79](https://github.com/Mehardeep79)
- LinkedIn: [Mehardeep Singh Sandhu](https://www.linkedin.com/in/mehardeep-singh-sandhu/)

