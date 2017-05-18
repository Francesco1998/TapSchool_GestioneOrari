-- phpMyAdmin SQL Dump
-- version 4.6.5.2
-- https://www.phpmyadmin.net/
--
-- Host: 127.0.0.1
-- Creato il: Mag 17, 2017 alle 15:50
-- Versione del server: 10.1.21-MariaDB
-- Versione PHP: 7.1.1

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Database: `databasetapschool`
--

-- --------------------------------------------------------

--
-- Struttura della tabella `classe`
--

CREATE TABLE `classe` (
  `ID` int(11) NOT NULL,
  `Aula` int(11) NOT NULL,
  `NomeCSV` varchar(8) NOT NULL,
  `Indirizzo` varchar(32) NOT NULL,
  `Anno` int(11) NOT NULL,
  `Sezione` char(1) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

-- --------------------------------------------------------

--
-- Struttura della tabella `lab`
--

CREATE TABLE `lab` (
  `ID` int(11) NOT NULL,
  `Nome` varchar(16) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

-- --------------------------------------------------------

--
-- Struttura della tabella `materia`
--

CREATE TABLE `materia` (
  `ID` int(11) NOT NULL,
  `Nome` varchar(16) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

-- --------------------------------------------------------

--
-- Struttura della tabella `ora`
--

CREATE TABLE `ora` (
  `ID` int(11) NOT NULL,
  `nOra` int(11) NOT NULL,
  `Giorno` int(11) NOT NULL,
  `IDmat` int(11) NOT NULL,
  `IDprof` int(11) NOT NULL,
  `IDclasse` int(11) NOT NULL,
  `IDlab` int(11) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

-- --------------------------------------------------------

--
-- Struttura della tabella `prof`
--

CREATE TABLE `prof` (
  `ID` int(11) NOT NULL,
  `Nome` varchar(16) NOT NULL,
  `Cognome` varchar(16) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

-- --------------------------------------------------------

--
-- Struttura della tabella `studente`
--

CREATE TABLE `studente` (
  `ID` int(11) NOT NULL,
  `Nome` varchar(16) NOT NULL,
  `Cognome` varchar(16) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Indici per le tabelle scaricate
--

--
-- Indici per le tabelle `classe`
--
ALTER TABLE `classe`
  ADD PRIMARY KEY (`ID`);

--
-- Indici per le tabelle `lab`
--
ALTER TABLE `lab`
  ADD PRIMARY KEY (`ID`);

--
-- Indici per le tabelle `materia`
--
ALTER TABLE `materia`
  ADD PRIMARY KEY (`ID`);

--
-- Indici per le tabelle `ora`
--
ALTER TABLE `ora`
  ADD PRIMARY KEY (`ID`),
  ADD KEY `IDclasse` (`IDclasse`),
  ADD KEY `IDlab` (`IDlab`),
  ADD KEY `IDmat` (`IDmat`),
  ADD KEY `IDprof` (`IDprof`);

--
-- Indici per le tabelle `prof`
--
ALTER TABLE `prof`
  ADD PRIMARY KEY (`ID`);

--
-- Indici per le tabelle `studente`
--
ALTER TABLE `studente`
  ADD PRIMARY KEY (`ID`);

--
-- AUTO_INCREMENT per le tabelle scaricate
--

--
-- AUTO_INCREMENT per la tabella `classe`
--
ALTER TABLE `classe`
  MODIFY `ID` int(11) NOT NULL AUTO_INCREMENT;
--
-- AUTO_INCREMENT per la tabella `lab`
--
ALTER TABLE `lab`
  MODIFY `ID` int(11) NOT NULL AUTO_INCREMENT;
--
-- AUTO_INCREMENT per la tabella `materia`
--
ALTER TABLE `materia`
  MODIFY `ID` int(11) NOT NULL AUTO_INCREMENT;
--
-- AUTO_INCREMENT per la tabella `ora`
--
ALTER TABLE `ora`
  MODIFY `ID` int(11) NOT NULL AUTO_INCREMENT;
--
-- AUTO_INCREMENT per la tabella `prof`
--
ALTER TABLE `prof`
  MODIFY `ID` int(11) NOT NULL AUTO_INCREMENT;
--
-- AUTO_INCREMENT per la tabella `studente`
--
ALTER TABLE `studente`
  MODIFY `ID` int(11) NOT NULL AUTO_INCREMENT;
--
-- Limiti per le tabelle scaricate
--

--
-- Limiti per la tabella `ora`
--
ALTER TABLE `ora`
  ADD CONSTRAINT `ora_ibfk_1` FOREIGN KEY (`IDclasse`) REFERENCES `classe` (`ID`),
  ADD CONSTRAINT `ora_ibfk_2` FOREIGN KEY (`IDlab`) REFERENCES `lab` (`ID`),
  ADD CONSTRAINT `ora_ibfk_3` FOREIGN KEY (`IDmat`) REFERENCES `materia` (`ID`),
  ADD CONSTRAINT `ora_ibfk_4` FOREIGN KEY (`IDprof`) REFERENCES `prof` (`ID`);

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
