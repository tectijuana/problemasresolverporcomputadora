# Cómo contribuir

Gracias por tu interés en mejorar este repositorio. Toda contribución es bienvenida — desde corregir un acento hasta proponer un problema nuevo para los capítulos de IA.

## Tipos de contribución

### Correcciones (prioridad alta)
- Errores en el enunciado de un problema
- Fórmulas LaTeX mal formateadas
- Links rotos en el README

### Mejoras
- Modernizar el contexto de un problema (precios, nombres de instituciones, referencias culturales)
- Mejorar la claridad del enunciado sin cambiar el problema matemático

### Nuevos problemas
- Proponer problemas para los capítulos 12–22 (extensión moderna)
- Cada propuesta debe incluir: enunciado completo, capítulo sugerido y justificación de por qué encaja

### Soluciones de referencia
- Agregar soluciones en Python, C, JavaScript u otro lenguaje moderno
- Se aceptan en carpeta `soluciones/capitulo##/problema_##.py` (o la extensión correspondiente)

## Proceso

1. **Abre un issue** antes de hacer cambios grandes — así alineamos el enfoque
2. **Haz un fork** del repositorio
3. **Crea una rama** descriptiva: `fix/cap05-p23-formula` o `feat/cap19-nuevo-problema`
4. **Haz tus cambios** respetando la convención de formato (ver abajo)
5. **Abre un Pull Request** con descripción clara de qué cambiaste y por qué

## Convención de formato

- Numeración: `**N.**` al inicio de cada problema
- LaTeX: solo `$formula$` inline — cero entornos `\begin{}`/`\end{}`
- Moneda en texto corrido: `\$` para evitar conflicto con delimitador LaTeX
- Encabezado Spencer (caps. 1–11): `> *Basado en el libro de Donald D. Spencer, Editorial Limusa, 1985*`
- Encabezado extensión (caps. 12–22): `> *Capítulo de elaboración propia — extensión moderna del libro de Donald D. Spencer para programadores mexicanos 2026*`

## Verificación rápida

```bash
# Contar problemas en un capítulo
grep -c '^\*\*[0-9]' capitulo##.md

# Verificar que no hay ambientes LaTeX prohibidos
grep -c '\\begin\|\\end{' capitulo##.md   # debe ser 0
```

## Código de conducta

Este proyecto se rige por el [Código de Conducta](CODE_OF_CONDUCT.md). Al participar, aceptas respetarlo.
