# 🎰 The High Roller's Network

## The Big Game

Welcome to Las Vegas Digital, the most ambitious online casino platform in the
making! We're building a revolutionary system to track our VIP relationships,
gaming hierarchies, and player networks. Just like Vegas itself, everything in
our world is connected, flowing from the top whales down to the everyday
players.

## The House Always Needs Structure

In our casino, every player is a node in an intricate network of relationships.
Think of it like our exclusive VIP referral system:

* The Casino (root node) sits at the top
* High Rollers (parent nodes) bring in their connections
* Regular players (child nodes) bring in their friends
* New players (leaf nodes) are just starting their journey

Here's how our current network looks:

```mermaid
flowchart TD
 A[Casino] --> B[High Roller Bob]
 A --> C[Slot King Carl]
 A --> D[Poker Queen Diana]
 B --> E[Player E]
 B --> F[Player F]
 B --> G[Player G]
 B --> H[Player H]
 D --> I[Player I]
 D --> L[Player L]
 D --> M[Player M]
 I --> J[Player J]
 J --> K[Player K]
 M --> N[Player N]
```

## Your Mission: Build The Ultimate Player Network System

We need a sophisticated API service that can manage our entire player network.
Here's what's at stake:

1. Welcome New Players to the Table
    * Add new players under their referrers
    * Track who brought whom to the casino
    * Maintain the referral chain integrity
2. Player Checkout
    * Handle players leaving the network
    * Maintain remaining connections
    * Clean historical data properly
3. VIP Host Reassignment
    * Transfer players between different VIP hosts
    * Update referral chains without losing history
    * Maintain commission structures
4. The Million Dollar Question - Network Tracking
    * This is where the big money is! Given any player in our network, we need
      to see their entire downline.

### For example

* Query the Casino's (A) entire network:
  * Example request:

    ```shell
    curl --url "https://mycasino.com/api/network/A/downline"
    ```

  * Example reponse

    ```json
    ["B","C","D","E","F","G","H","I","J","K","L","M","N"]
    ```

    or 

    ```XML
    <nodes>
      <node>B</node>
      <node>C</node>
      <node>D</node>
      <node>E</node>
      <node>F</node>
      <node>G</node>
      <node>H</node>
      <node>I</node>
      <node>J</node>
      <node>K</node>
      <node>L</node>
      <node>M</node>
      <node>N</node>
    </nodes>
    ```

    >(Every player in the house!)

* Query Poker Queen Diana's (D) network:
  * Example request:

    ```shell
    curl --url "https://mycasino.com/api/network/D/downline"
    ```

  * Example reponse

    ```json
    ["I","J","K","L","M","N"]
    ```

    > (Everyone she and her referrals brought in)

* Query Slot King Carl's (C) network::
  * Example request:

    ```shell
    curl --url "https://mycasino.com/api/network/C/downline"
    ```

  * Example reponse

    ```json
    []
    ```

    > (Looks like Carl needs to step up his game!)

## The Tech Stack (House Rules)

Build your system using:

* Spring Boot (latest) - as reliable as our slot machines
* Java 17+ - faster than a dealer's shuffle
* Any RDBMS/NoSQL - your chips, your choice
* Maven/Gradle - house tools

## Requirements (Casino Compliance)

Your API must:

* Follow REST best practices (we run a clean house)
* Support both JSON and XML (for our international players)
* Use proper HTTP status codes (like our precise payout systems)
* Use propper HTTP Verbs (We speak like propper Genttlemen or Ladies)
* Include proper documentation (house rules must be clear)

## Time to Show Your Hand

You have 5 days to build this system. Like any good poker player, show us:

* How to run it
* How to use it
* How to test it

Bonus chips if you creativity and **WOW!! Effect!**, we like to be surprise

Remember: What happens in the API, stays in the API. Keep it clean, keep it
professional, and make it scale like a Vegas weekend.

Good luck, and may the odds be ever in your favor! 🎲
