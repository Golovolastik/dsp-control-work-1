# DSP Control Work 1

## Описание
Контрольная работа по цифровой обработке сигналов (ЦОС) - часть 1.

## Задание
Обработка гармонических и полигармонических сигналов с использованием дискретного преобразования Фурье (DFT) и быстрого преобразования Фурье (FFT).

## Реализованные функции

### Основные функции DFT
- `make_sin_cos_tables(N)` - создание таблиц sin/cos
- `dft_harmonic(x, N, j, cos_table, sin_table)` - DFT для отдельной гармоники
- `spectrum_all(x, N, cos_table, sin_table)` - полный спектр сигнала
- `reconstruct_from_A_phi(A, phi, N)` - восстановление сигнала по спектру

### FFT реализация
- `my_fft(x)` - собственная реализация FFT (Cooley-Tukey)
- `my_ifft(X)` - обратное FFT
- `compare_fft_implementations(x)` - сравнение с NumPy FFT

### Цифровые фильтры
- `low_pass_filter(x, cutoff_freq, N)` - НЧ-фильтр
- `high_pass_filter(x, cutoff_freq, N)` - ВЧ-фильтр
- `band_pass_filter(x, low_cutoff, high_cutoff, N)` - полосовой фильтр
- `band_stop_filter(x, low_cutoff, high_cutoff, N)` - режекторный фильтр

### Демонстрационные функции
- `demo(N, J, plot)` - основная демонстрация DFT и восстановления
- `demo_filters(N)` - демонстрация цифровых фильтров
- `comprehensive_demo()` - комплексная демонстрация всех возможностей

## Структура проекта
```
├── src/
│   └── dft_demo.ipynb    # Основной Jupyter notebook
├── README.md             # Этот файл
└── .gitignore           # Исключения для Git
```

## Требования
- Python 3.7+
- NumPy
- Matplotlib
- Jupyter Notebook

## Запуск
1. Откройте `src/dft_demo.ipynb` в Jupyter Notebook
2. Запустите все ячейки последовательно (Kernel → Restart & Run All)
3. Или запустите отдельные демонстрации:
   - `demo(N=128, J=30, plot=True)` - основное задание
   - `demo_filters(N=128)` - фильтрация
   - `comprehensive_demo()` - полная демонстрация

## Результаты
- Реализация DFT с использованием таблиц sin/cos
- Восстановление сигналов по спектру (с фазами и без фаз)
- Собственная реализация FFT
- Цифровая фильтрация в частотной области
- Сравнение с библиотечными функциями NumPy
- Визуализация результатов на едином канвасе

## Автор
Студент БГУИР, 5 курс
