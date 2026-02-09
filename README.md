# 🧠 Federated AI Predictive Network for Aerospace Medicine

> Harvard Medical School · AI in Healthcare: From Strategies to Implementation  
> Capstone Project — **Prefinalista**  
> Edward Adalid Pereira · Diciembre 2025

---

## 📋 Resumen Ejecutivo

Plataforma de inteligencia artificial federada diseñada para las **23 bases aéreas de la Fuerza Aérea Argentina**, orientada a cerrar brechas diagnósticas entre el Hospital Aeronáutico Central y las unidades sanitarias periféricas.

**Problema:** Las bases periféricas tienen capacidad diagnóstica limitada, lo que genera traslados innecesarios (costosos, riesgosos) y diagnósticos tardíos en poblaciones geográficamente aisladas.

**Solución:** Dos módulos de IA integrados que permiten predecir eventos médicos y diagnosticar patologías raras sin centralizar datos sensibles.

## 🏗️ Arquitectura

```
┌─────────────────────────────────────────────────┐
│              MÓDULO A: Transfer Learning         │
│  Predicción de eventos médicos críticos          │
│  en bases periféricas con datos parciales        │
│                                                  │
│  Input:  Datos clínicos limitados (periféricas)  │
│  Model:  Gradient Boosting + Neural Networks     │
│  Output: Score de riesgo + recomendación         │
└─────────────────────┬───────────────────────────┘
                      │
              Datos federados (no se comparten)
                      │
┌─────────────────────┴───────────────────────────┐
│           MÓDULO B: Federated Learning           │
│  Diagnóstico colaborativo de patologías          │
│  aeroespaciales raras                            │
│                                                  │
│  Input:  Modelos locales de cada base            │
│  Model:  Federated averaging + diff. privacy     │
│  Output: Modelo global sin exponer datos         │
└─────────────────────────────────────────────────┘
```

## 🎯 Objetivos

| Métrica | Situación actual | Objetivo |
|---------|-----------------|----------|
| Traslados innecesarios | ~200/año estimados | **-40%** |
| Tiempo diagnóstico (periféricas) | 7-15 días | **< 48 horas** |
| Cobertura diagnóstica | Solo Hospital Central | **23 bases** |
| Privacidad de datos | Centralización requerida | **Zero data sharing** |

## 🔬 Metodología

### Datos
- **30+ años** de registros del sistema INMAE
- **23 bases aéreas** con datos heterogéneos
- Patologías aeroespaciales: hipoxia, cinetosis, barotrauma, fatiga de vuelo, DCS

### Modelos
- **Gradient Boosting** (XGBoost) para predicción de riesgo con datos tabulares
- **Redes Neuronales** para detección de patrones complejos
- **SHAP** (SHapley Additive exPlanations) para explicabilidad clínica
- **Federated Averaging** para entrenamiento distribuido con privacidad diferencial

### Implementación (3 fases, 18 meses)

| Fase | Duración | Alcance |
|------|----------|---------|
| **Fase 1:** Piloto | 6 meses | 3 bases principales + Hospital Central |
| **Fase 2:** Expansión | 6 meses | 12 bases adicionales |
| **Fase 3:** Escala completa | 6 meses | 23 bases + evaluación de impacto |

## 📊 Explicabilidad

La explicabilidad clínica es central al diseño. Cada predicción incluye:

- **SHAP values** para cada variable de entrada
- **Ranking de factores** contribuyentes al score de riesgo
- **Comparación con población** de referencia (pilotos del Hospital Central)
- **Recomendación accionable** para el médico de la base periférica

## 🏥 Contexto Clínico

Este proyecto nace de 12 años de experiencia como médico militar en el sistema de salud aeroespacial argentino:

- **Instructor de cámara hipobárica** con 236 pilotos evaluados ([publicación indexada](https://pesquisa.bvsalud.org/portal/resource/pt/biblio-910830))
- **Médico aeroevacuador** con experiencia en Antártida y alta montaña
- **Jefe de Informática Médica** del Centro Asistencial Retiro (50K+ usuarios INMAE)
- **Investigación publicada** en hipoxia de vuelo y cinetosis

## 📚 Referencias del programa

- **Faculty Director:** Andrew Beam, PhD (Harvard Medical School)
- **Dean for External Education:** David H. Roberts, MD
- **Programa:** AI in Health Care: From Strategies to Implementation
- **Duración:** Octubre — Diciembre 2025 (8 semanas)
- **Certificado:** [Verificar](https://certificates.emeritus.org/b3819339-5f70-464c-9d8f-fa56573616fb)

## 🔗 Links

- 🌐 [edward.com.ar](https://edward.com.ar)
- 💼 [LinkedIn](https://linkedin.com/in/itedward/)
- 🆔 [ORCID: 0009-0005-0220-3586](https://orcid.org/0009-0005-0220-3586)
- 🔬 [ResearchGate](https://www.researchgate.net/profile/Edward-Pereira-4)

---

## ⚖️ Licencia

Este repositorio contiene la documentación y diseño conceptual del proyecto capstone. El código fuente de implementación pertenece al ámbito institucional de la Fuerza Aérea Argentina.

MIT License © 2025 Edward Adalid Pereira
