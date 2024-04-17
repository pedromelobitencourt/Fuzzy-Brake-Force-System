# Fuzzy Brake Force Determination System

This repository contains a Jupyter Notebook implementing a fuzzy system to determine the brake force of a vehicle based on the distance from the car in front and its velocity.

This project is part of an AI course at the Federal Center for Technological Education of Minas Gerais (CEFET-MG).

## Notebook Overview

The notebook implements a fuzzy system using the scikit-fuzzy library. Linguistic variables for distance and velocity are defined with automatic membership functions. The output linguistic variable, representing brake force, ranges from 0 to 100 and is divided into five linguistic terms: very_weak, weak, moderate, strong, and very_strong.

### Linguistic Variable Inputs

- **Distance**: Five terms are defined: very_close, close, moderate, far, and very_far.
- **Velocity**: Five terms are defined: very_slow, slow, moderate, fast, and very_fast.

### Linguistic Variable Outputs

- **Brake Force**: Five terms are defined: very_weak, weak, moderate, strong, and very_strong.

## Fuzzy Max-Min Rules

The notebook compares Fuzzy Max-Min and Fuzzy Max-Prod functions for combining rules

In Fuzzy Max-Min, rules are combined using the operator MIN. This means that the lowest activation rule will be selected as the contribution of the corresponding rule to the final output. The activation of each rule is determined by how much it matches the input values. The MIN operator ensures that the contribution of each rule is limited by the lowest activation rule. As a result, Fuzzy Max-Min tends to produce a more conservative output, as the lowest activation of a rule restricts its influence on the final output.

## Fuzzy Max-Prod Rules

In Fuzzy Max-Prod, rules are combined using the PROD (product) operator. This means that the activations of all rules are multiplied to determine the contribution of each rule to the final output. Each rule's activation is determined by how much it matches the input values. The PROD operator allows all rules to contribute to the final output, and rules with higher activation will have a proportionally greater contribution. This can result in a more aggressive output, as all rules have the opportunity to influence the output and rules with higher activation will have a proportionally greater contribution.

### Analysis

Both approaches have their advantages and are suited to different problem domains. Fuzzy Max-Min tends to be more conservative and cautious in its output, while Fuzzy Max-Prod can be more aggressive and decisive. The choice between the two depends on the specific requirements of the application and the desired behavior of the system.

## Usage

Simply open the Jupyter Notebook and execute the cells to explore the implementation of the fuzzy system.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

