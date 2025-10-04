
A circuit network is a red or green wire which connects 2 or more buildings:

![[Screenshot_20251004_105857.png]]

You create red or green wires by using the buttons on the toolbar:

![[Screenshot_20251004_110403.png]]

Or their keyboard shortcuts (<kbd>Alt+R</kbd> and <kbd>Alt + G</kbd> , by default)

These wires have a limited range, but can be connected to power poles to extend their range:

![[Screenshot_20251004_110818.png]]

Circuit networks carry collections of numbers called signals, which can be viewed by hovering the mouse over a power pole connected to the network:

![[Screenshot_20251004_111121.png]]

Or by connecting it to the input of a decider combinator and clicking on it:

![[Screenshot_20251004_111315.png]]

Or finally by clicking on another connected machine and hovering over the circuit network number:

![[Screenshot_20251004_111536.png]]

Signals can be added to a circuit network by connecting a constant combinator with some signals set:

![[Screenshot_20251004_111838.png]]

Or by connecting a chest with "Read contents" checked:

![[Screenshot_20251004_111946.png]]

And it's not just chests, many buildings in Factorio can be connected to the circuit network and have their contents read.

![[Screenshot_20251004_112742.png]]

When multiple buildings are contributing signals to the same network, the numbers for each signal get **added together**.

As an example, if I have a chest containing 100 concrete

![[Screenshot_20251004_113207.png]]

connected to a constant combinator set to 50 concrete and 50 coal

![[Screenshot_20251004_113310.png]]

The resulting circuit network will have 150 concrete and 50 coal

![[Screenshot_20251004_113346.png]]

Red and green wires, however, and never connected together; even when both connected to the same building.

![[Screenshot_20251004_113844.png]]

This can be handy for routing multiple circuit networks long distances along big power poles, or for connecting a combinator or building to two different networks.

These signals can then be used to control the behavior of buildings which are connected to a circuit network. For example, inserters can be enabled/disabled based on the value of a signal on the network.

![[Screenshot_20251004_114620.png]]

This inserter will only take items from the chest when there are more than 50 concrete in it.

Inserters can also have their filters or stack size controlled by the circuit network by checking the appropriate boxes, which gives the circuit network essentially complete control over how an inserter moves items, since it can control which items it moves, how many it moves, and when it moves them.

Other buildings can similarly have many aspects of their behavior controlled by circuit network, so it's worth poking around the "Circuit connection" options for each building you might want to control.

However, the enable/disable option can only check the value of a single signal; to write more complex conditions, you need combinators.