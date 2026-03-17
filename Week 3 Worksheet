# Visualize the Schaefer growth curve (parabola)

import numpy as np
import matplotlib.pyplot as plt

# Parameters
g = 0.4
K = 1500

# Define the Schaefer growth function
def schaefer_growth(S, g, K):
    return g * S * (1 - S / K)

# Generate stock values
S = np.linspace(0, K, 200)
G = schaefer_growth(S, g, K)

# Plot the growth curve
plt.figure(figsize=(12,6))
plt.plot(S, G, 'b-', linewidth=2, label=r'$G(S) = gS(1 - S/K)$')

# Mark MSY point
S_msy = K / 2
G_msy = schaefer_growth(S_msy, g, K)
plt.plot(S_msy, G_msy, 'ro', markersize=12, label=f'MSY: S={S_msy:.0f}, G={G_msy:.0f}')

# Mark carrying capacity
plt.axvline(x=K, color='green', linestyle='--', alpha=0.7, label=f'K = {K}')

# Labels and title
plt.xlabel('Stock S (tonnes)', fontsize=12)
plt.ylabel('Growth G(S) (tonnes/year)', fontsize=12)
plt.title('Schaefer Growth Model: A Downward Parabola', fontsize=14)

# Legend and grid
plt.legend(fontsize=11)
plt.grid(True, alpha=0.3)

# Show plot
plt.show()

# Key observations
print("Key Observations:")
print("- Growth is a quadratic function of stock (parabola)")
print("- Parabola opens downward (negative coefficient on S^2)")
print(f"- Maximum at vertex: S = K/2 = {S_msy:.0f} tonnes")
print(f"- MSY = gK/4 = {g*K/4:.0f} tonnes/year")
