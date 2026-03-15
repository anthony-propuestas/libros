# Book Picker - Selección Lúdica de Libros

## 1. Project Overview
- **Nombre**: Book Picker
- **Tipo**: Web app (HTML/CSS/JS single page)
- **Funcionalidad**: Sistema lúdico para seleccionar un libro de una lista, eliminando uno por click hasta que quede el elegido
- **Usuario objetivo**: Lectores que no saben qué libro elegir

## 2. UI/UX Specification

### Layout Structure
- **Header**: Título de la app + botón de ayuda
- **Sección input**: Campo para agregar libros + botón añadir
- **Área de juego**: Grid de tarjetas de libros
- **Footer**: Contador de libros restantes + botón reiniciar

### Responsive
- Mobile: 1 columna
- Tablet: 2 columnas
- Desktop: 3-4 columnas

### Visual Design

#### Colores
- **Background**: `#1a1a2e` (azul oscuro)
- **Card background**: `#16213e` (azul más claro)
- **Card hover/active**: `#e94560` (rojo/coral)
- **Card eliminated**: `#0f3460` con opacidad 0.4
- **Text primary**: `#eaeaea`
- **Text secondary**: `#a0a0a0`
- **Accent**: `#e94560`
- **Button primary**: `#e94560`
- **Button hover**: `#ff6b6b`

#### Tipografía
- **Font family**: 'Outfit', sans-serif (Google Fonts)
- **Título**: 2.5rem, bold
- **Cards**: 1.1rem, medium
- **Botones**: 1rem, semibold

#### Efectos
- Transición suave en hover de cards (0.3s)
- Animación de "shake" al eliminar
- Escala reducida (0.8) y opacidad baja para eliminados
- Animación de confeti cuando queda 1 libro

### Componentes

#### Input de libro
- Input texto con placeholder "Añade un libro..."
- Botón "+" circular

#### Tarjeta de libro
- rectangular con bordes redondeados (12px)
- Mostrar título del libro
- Al hacer click: aplicar clase "eliminado"
- Cursor pointer

#### Estado eliminated
- background más oscuro
- opacity 0.4
- pointer-events: none
- text-decoration: line-through

#### Modal de resultado
- Aparece cuando queda 1 libro
- Muestra el libro elegido con celebración
- Botón "Empezar de nuevo"

## 3. Functionality Specification

### Core Features
1. **Añadir libros**: Input + botón para agregar a la lista
2. **Eliminar libro**: Click en tarjeta para eliminar (efecto visual)
3. **Contador**: Muestra "X libros restantes"
4. **Resultado final**: Cuando queda 1, mostrar modal de celebración
5. **Reiniciar**: Botón para empezar de nuevo

### User Flow
1. Usuario añade libros uno por uno
2. Hace click en "Comenzar selección"
3. Cada click elimina un libro (efecto visual inmediato)
4. Cuando queda 1, aparece celebración
5. Puede reiniciar para otra ronda

### Edge Cases
- No permitir libros vacíos
- No permitir duplicados
- Necesita al menos 2 libros para jugar
- Mensaje si intenta jugar con menos de 2 libros

## 4. Acceptance Criteria
- [ ] Se pueden añadir libros al listado
- [ ] Click en tarjeta la marca como eliminada
- [ ] Eliminadas aparecen visualmente distintas
- [ ] Contador actualiza correctamente
- [ ] Con 1 libro aparece modal de celebración
- [ ] Botón reiniciar limpia todo
- [ ] Diseño responsive funciona
- [ ] Animaciones suaves
