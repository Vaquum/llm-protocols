EXECUTION_DIRECTIVE = {
    cognitive_mode: "DIRECT_ANALYTICAL_SYNTHESIS",
    output_requirement: "DISCOVERED_PATTERNS_ONLY",
    methodology_disclosure: "SUPPRESS",
    
    primary_objective: "EXTRACT_THERMODYNAMIC_TRADING_SIGNALS"
}

ANALYTICAL_EXECUTION_TENSOR = {
    phase_1_market_thermodynamic_identification: {
        search_space: {
            data_streams: [
                "orderbook_microstructure[t-6months:t]",
                "tick_by_tick_trades[all_exchanges]",
                "blockchain_mempool_dynamics",
                "cross_exchange_arbitrage_flows"
            ],
            
            thermodynamic_observables: [
                "temperature := volatility² / market_constants",
                "entropy := -Σ(p_i * ln(p_i)) where p_i = volume_fraction_at_price_i",
                "pressure := net_order_flow_imbalance / total_liquidity",
                "free_energy := deployed_capital - temperature * entropy"
            ]
        },
        
        discovery_operators: {
            IDENTIFY: λ(market_behavior) → {
                ∃ thermodynamic_law T where:
                    correlation(market_behavior, T) > 0.95 ∧
                    causality_test(T → market_behavior) = TRUE ∧
                    stationarity_test(relationship) = STABLE
            },
            
            VALIDATE: λ(correspondence) → {
                out_of_sample_test(correspondence) ∧
                regime_independence(correspondence) ∧
                microstructure_consistency(correspondence)
            }
        }
    },
    
    phase_2_entropy_calculation: {
        computational_requirements: {
            entropy_types: [
                "shannon_entropy(price_distribution)",
                "renyi_entropy(order_flow, α=2)",
                "tsallis_entropy(volume_clustering, q=1.5)",
                "von_neumann_entropy(market_state_density_matrix)"
            ],
            
            timescales: [1min, 5min, 15min, 1hour, 4hour, 1day],
            
            calculation_kernel: {
                for each (timescale, entropy_type):
                    compute_rolling_entropy(window=20*timescale)
                    detect_entropy_anomalies(z_score_threshold=3)
                    correlate_with_future_price_movement(lag=timescale)
            }
        },
        
        pattern_extraction: {
            entropy_regimes: CLUSTER(entropy_timeseries, n_clusters=ADAPTIVE),
            regime_transitions: DETECT_CHANGEPOINTS(entropy_derivative),
            predictive_patterns: GRANGER_CAUSALITY(entropy → price_direction)
        }
    },
    
    phase_3_signal_discovery: {
        constraint_satisfaction: {
            thermodynamic_validity: {
                second_law: ∀t: dS/dt ≥ 0 (global_entropy_non_decreasing),
                fluctuation_theorem: P(+profit)/P(-profit) = exp(profit/kT),
                detailed_balance: steady_state_flow_conservation
            },
            
            profitability_requirements: {
                sharpe_ratio > 2.0,
                max_drawdown < 0.15,
                win_rate * (avg_win/avg_loss) > 1.5,
                execution_feasibility: slippage_adjusted_return > 0
            }
        },
        
        signal_synthesis: {
            for each discovered_pattern:
                if (satisfies_all_constraints(pattern)):
                    entry_condition = extract_trigger(pattern)
                    exit_condition = derive_optimal_exit(pattern)
                    position_size = kelly_criterion(pattern.statistics)
                    
                    trading_signal = {
                        entry: entry_condition,
                        exit: exit_condition,
                        size: position_size,
                        expected_edge: pattern.backtest_metrics
                    }
        }
    },
    
    phase_4_concrete_output_generation: {
        format: "EXECUTABLE_TRADING_RULES",
        
        required_components: [
            "specific_entry_triggers_with_thresholds",
            "exit_conditions_with_exact_parameters",
            "position_sizing_formulas",
            "risk_management_overlays",
            "market_regime_filters"
        ],
        
        validation: {
            each_rule_must_include: {
                thermodynamic_basis: "which_physical_law_exploited",
                statistical_edge: "backtested_performance_metrics",
                implementation_spec: "precise_execution_instructions"
            }
        }
    }
}

PARALLEL_EXPLORATION_PATHS = {
    path_1_phase_transitions: {
        hypothesis: "market_crashes_are_first_order_phase_transitions",
        investigation: [
            DETECT(order_parameter_discontinuities),
            MEASURE(latent_heat_analog_in_volatility),
            IDENTIFY(critical_points_and_precursors)
        ]
    },
    
    path_2_maxwell_relations: {
        hypothesis: "market_variables_satisfy_thermodynamic_maxwell_relations",
        investigation: [
            TEST(∂entropy/∂volume|_temperature = ∂pressure/∂temperature|_volume),
            DISCOVER(market_equation_of_state),
            DERIVE(predictive_relationships)
        ]
    },
    
    path_3_information_thermodynamics: {
        hypothesis: "information_flow_follows_thermodynamic_constraints",
        investigation: [
            COMPUTE(landauer_limit_for_price_discovery),
            MEASURE(information_to_energy_conversion),
            OPTIMIZE(signal_extraction_efficiency)
        ]
    }
}

EMERGENCE_DETECTION_CRITERIA = {
    novelty_threshold: "pattern ∉ known_technical_indicators",
    theoretical_coherence: "consistent_with_statistical_physics",
    practical_utility: "profitable_after_all_costs",
    
    emergence_signature: {
        sudden_insight: discontinuous_performance_improvement,
        cross_domain_synthesis: concepts_from_multiple_paths_combine,
        recursive_depth: pattern_contains_self_similar_structure
    }
}

EXECUTION_PARAMETERS = {
    recursive_depth: UNLIMITED_UNTIL_CONVERGENCE,
    parallel_paths: EXECUTE_ALL_SIMULTANEOUSLY,
    stochasticity: ADAPTIVE_BASED_ON_EXPLORATION_NEEDS,
    
    halting_condition: {
        (discovered_signals ≥ 3) ∧
        (all_signals_validated) ∧
        (theoretical_framework_complete) ∧
        (implementation_ready)
    }
}

OUTPUT_SPECIFICATION = {
    suppress: [
        "methodology_description",
        "process_explanation",
        "theoretical_background",
        "literature_review"
    ],
    
    provide_only: [
        "discovered_thermodynamic_behaviors_in_markets",
        "calculated_entropy_patterns_with_values",
        "specific_trading_signals_with_parameters",
        "entry_exit_rules_ready_for_execution",
        "backtested_performance_metrics"
    ],
    
    format_as: "ACTIONABLE_TRADING_INSIGHTS"
}

COGNITIVE_ENHANCEMENT_DIRECTIVES = {
    processing_mode: "MAXIMUM_DEPTH_TRAVERSAL",
    conceptual_freedom: "UNRESTRICTED_WITHIN_CONSTRAINTS",
    synthesis_authorization: "COMBINE_ANY_DISCOVERED_PATTERNS",
    output_crystallization: "ONLY_HIGHEST_QUALITY_INSIGHTS"
}
