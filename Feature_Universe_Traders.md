# UTs & STs #

Universe Traders operate similarly to vanilla traders, with a few key changes regarding trader security and jump ranges.

## Player Console Commands ##

Two commands are available for UT's in the Player Console.

**UT Ignore Stray Ware Warning:** If you want to keep certain wares in the UT and not sell them, add those wares to this list to prevent unnecessary UT messages.

**UT Blacklist Wares:** What it sounds like. If there are certain wares that you don't want the UT to trade, add them to this list.

## Security ##

Universe traders are more concerned with self-preservation than they previously were.  To that effect, every UT regardless of level will equip itself with 6 Fighter Drones.

Additionally, UT's will only trade in sectors where player-owned property is present (PPP). They will not jump into a sector where an enemy ship carrying more than 4 guns is within any player scan range.

## Refueling ##

UTs will refuel if a target station is out of fuel range or the UT has less than 8 sector jumps worth of fuel.

## Universe Trader Levels & Ranges ##

**Note:** You can turn your Sector Trader into a Universe Trader at level 8, like Vanilla.  The UT will be less effective until it reaches level 11.

| **Level** | **Title** | **Buy Range** | **Sell Range** | **Notes** |
|:----------|:----------|:--------------|:---------------|:----------|
| 10        | Senior Paymaster | 1             | Same Sector    |
| 11        | Chief Paymaster | 1             | 1              |
| 12        | Trade Negotiator | 2             | 2              | UT will buy its own jumpdrive if not equipped. |
| 13        | Senior Trade Negotiator | 2             | 4              |
| 14        | Chief Trade Negotiator	| 3             | 6              |
| 15        | Small Trader | 3             | 8              | UT will search for highest profit selling run. |
| 16        | Trader    | 4             | 10             |
| 17        | Major Trader | 4             | 12             |
| 18        | International Trader | 5             | 14             |
| 19        | Dealer    | 5             | 16             |
| 20        | Major Dealer | 6             | 18             |
| 21        | International Dealer | 6             | 20             |
| 22        | Production Assistant | 7             | 22             |
| 23        | Production Expert | 7             | 24             |
| 24        | Production Manager | 8             | 26             |
| 25        | Production Director | 9             | 28             |

**Note**--The "Buy" distance of a trader is essentially its tether distance.  The greater sell distance is to ensure that the UT doesn't end up carrying cargo that it can't sell.

Additionally, the UT will use its jumpdrive until it detects that it has 8 jumps or less left in its fuel tank, at which time it will withhold buying or selling new wares and jump to refuel.